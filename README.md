# ABrennaman
A Campaign Website for Albert Brennaman, Running for Constable in Fayette County, Kentucky




# How to Convert Sass files to CSS

1. Divide your page into containers
      * <div class="container"></div>

2. Insert the text in the structure you want (headings/paragraphs, etc)

3. Once the foundation is set up, use BootStraps documentation to apply formatting
    * See https://getbootstrap.com/docs/4.1/getting-started/introduction/



# Instructions for Setting up Browser-Sync

This experiment introduces sass and browser-sync.

We installed sass and browser-sync for the entire project
(that is, in package.json in the project root) so that
we can use them again in later experiments.

First, run this command from the root of the project:

$ npm install

This pulls in the necessary dependencies.

From now on, our commands assume we are in the Sass experiment
directory. Go there with:

$ cd sass

Next, to see sass in action,

1. In the terminal, run:

$ ../node_modules/.bin/sass input.scss output.css --watch

This watches input.scss for changes, and runs sass when a
change is detected.

This terminal tab needs to remain open so that the watch
continues to run.

(cmd + t opens a new tab in terminal with
the same working directory)

2. Next, in your editor, make a change to input.scss.

The watch command should run sass to rebuild output.css
and output.css.map.

Next, to see Browser-sync in action:

3. Open a new terminal (cmd + t) and make sure you're in the sass directory. Then type:

$ ../node_modules/.bin/browser-sync start --server --files "output.css"

This starts browser-sync in server mode so that it will
deliver HTML pages. A new tab should open in your browser.
This tab is connected to browser-sync and should automatically
refresh when the watched files (output.css) change.

Make another change to input.scss to see first sass, then browser-sync
react to the update.
