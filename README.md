GraphWiz Dot Viewer
===================

A GTK based viewer for dot files.
Adapted from `xdot.py` by Jose Fonseca.

## Features from xdot

+ Pan and Zoom
+ Center on node
+ Follow edges
+ Automatic refresh when file changed

**N.B.:** URL links have been removed to accommodate other features.

## Features added

+ Node regex search
+ Side panel showing contents of nodes
+ Better refresh support using `inotify`


## TODO

+ use GIO for IO and for file watches
+ Complete rewrite of parser reusing [pygraphviz](http://networkx.lanl.gov/pygraphviz)
+ Advanced open:
  - Open dot file
  - Open xdot file
  - Filter to be used
  - Get from command: this would prompt for a command to execute to generate the graph to be displayed.
    Refresh will re-run the command.
    Save would always prompt for a location and dump the generated dot.
+ Modes:
  - View: the current one. Allows for exploration, search.
  - Edit: would allow to modify the model (attributes) on the fly, saving the modifications to file.
+ Options:
  - watch = auto reload on changes (cannot be switched off at the moment)
  - GraphViz filter to use (maybe put this as a combo in toolbar)
  - names of extra attributes to show + defaults
  - enable/disable animations
  - colors/style of highlights
+ Embedded text editor for source (with jump-to-line?)
+ Status OSD: loading/layout/reloading/error...
+ Stop/kill button
+ Search options (search bar?): regex, fields ...
+ Update animation: delete/add/move identifying nodes by id (not very reliable but can be useful)
+ General overlay mechanism for annotations: url/extra-contents/flags
+ Pressing CTRL shows if node has url, ctrl+click jumps to url
+ keys to highlight topological features: successors/predecessors...
+ Advanced side pane with content parsing:
  * booleans (flags)
  * markdown
  * HTML
  * plain text
  * JSON
  * Filenames (xdg-open/preview for plain-text and pictures)
  * nested dot graphs (?)
+ Double click triggers the default action on default extra attrib (`contents`?)
+ Attributes in side pane
+ Ability to modify attributes from side pane and save to file (?)

