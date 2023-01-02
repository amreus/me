# Keg Help Text
NAME
keg - create and manage knowledge exchange graphs

	ALIASES
keg (kn)

	SYNOPSIS
	keg COMMAND

	COMMANDS
e|edit          - choose and edit a specific node (default)
	help            - display help similar to man page format
	conf            - manage conf in C:\Users\Jim\AppData\Roaming\keg\config.yaml
	var             - cache variables in C:\Users\Jim\AppData\Local\keg\vars
	dex|index       - work with index (`dex`) files
	c|create        - create and edit content node
	current         - show the current keg
	d|dir|directory - print path to directory of current keg or node
	del|rm|delete   - delete node from current keg
	last            - show info about last created node
	changed|changes - show most recent n node changes
	title|titles    - find titles containing regular expressions
	init            - initialize current working dir as new keg
	rand|random     - edit random node, gamify content editing
	import          - import nodes into current keg
	grep            - grep regular expression out of all nodes
	view            - view a specific node
	columns         - print the number of columns resolved
	url|link        - print link to specific node
	tags|tag        - add node to the tags index

	SHORTCUTS
	set    - var set
	unset  - var unset
	get    - var get
	sample - create sample

	DESCRIPTION
	The keg (kn) command is for personal and public knowledge management as a
	Knowledge Exchange Graph (sometimes called "personal knowledge graph" or
			"zettelkasten"). Using keg (kn) you can create, update, search, and
	organize everything that passes through your brain that you may want to
	recall later, for whatever reason: school, training, team knowledge, or
	publishing a paper, article, blog, or book.

	Getting Started

	The steps to create your first KEG directory are below, but first a
	little about the structure of this directory, which does not necessarily
	require this keg (kn) command to create and maintain.

	A KEG directory (aka "keg") is just a directory containing a keg YAML
	file and a number of directories that have a README.md file called
	content nodes. A node directory must have an incrementing integer
	name as would be used in a database table. A keg usually also has a dex
	directory containing at least two files:

	1. Latest changes dex/changes.md
	2. All nodes by ID dex/nodes.tsv

	The keg (kn) command keeps these files up to date.

	A special zero node is used by convention as a target for links to
	nodes that have yet to be created.

	Okay, here are the specific steps to get started by creating your first
	keg directory. If you plan on using Git or GitHub hold off on doing
	anything with git for now.

	1. Create a directory and change into it
	2. Run the keg (kn) init command
	3. Update the YAML file it opens
	4. Exit your editor
	5. List contents of directory to see what was created
	6. Run the keg (kn) create sample command to create your first node
	7. Read and understand the sample
	8. Exit your editor
	9. Check your index with keg (kn) changes or keg (kn) titles
10. Repeat 6-9 creating several nodes (optionally omitting sample)
	11. Search titles with the keg (kn) titles command
	12. Edit node with title keywords with keg (kn) edit WORD command
	13. Edit node with grep regexp matches with keg (kn) grep WORD command
14. Notice that keg (kn) edit is the default (ex: keg (kn) WORD)

	Git and GitHub

	It's important when using Git that either the remote git repo has been
	fully created (so that git pull will work) or that git has not been run
	at all (no .git directory). Otherwise, keg (kn) will attempt to pull
	and fail. These instructions assume the reader understands git and the gh
	commands.

	Here are the steps to follow when Git and GitHub are wanted. They are
	essentially the same as Getting Started but include creating a GitHub
	repo with the gh command afterward.

	1. Create a directory and change into it
	2. Run the keg (kn) init command
	3. Update the YAML file it opens
	4. Exit your editor
	5. Create and push as Git repo with gh repo create
	6. Continue with steps 9+ from Getting Started

	Alternatively, one can simply create a GitHub repo from the web site and
	git clone it down to the local machine and then run keg (kn) init from
	within it.

	Learning KEG Markup Language

	Use the keg (kn) create sample command to automatically create a new
	content node sample that introduces the KEG Markup Language (KEGML). You
	can delete it later after reading it. Or, you can use it instead of just
	keg (kn) create (which gives you a blank) to help you remember how to
	write KEGML until you get proficient enough not to have to look it up
	every time.

	For more about the emerging KEG 2023-01 specification and how to create
	content that complies for knowledge exchange and publication (while we
			work more on linting and validation within the keg (kn) command) have a
	look at <https://github.com/rwxrob/keg-spec>

	CONTACT
	Site:   rwxrob.tv
	Source: git@github.com:rwxrob/keg.git
	Issues: https://github.com/rwxrob/keg/issues

	LEGAL
	keg (v0.9.2) Copyright 2022 Robert S Muhlestein
	License Apache-2.0

