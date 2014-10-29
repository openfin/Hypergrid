#OpenFin Grid
The OpenFin Grid control is a canvas based open source general purpose grid. The origin of this project is to address the Finance community's desire for a high performance, million row data-grid. At the moment, its in an alpha stage and still has a significant amount of work to be completed. These include bug-fixes/features/automated testing/etc.  Please try it out and let us know what you think.

## PluggableGridBehaviors
The design makes no assumptions about the data you wish to view which
allows for external data sources as well as external manipulation and
analytics.  Manipulations such as sorting, aggregation, and grouping 
can be achieved using external best of breed high-performant real time tools 
designed for such purposes.  

## Getting Started
1. Make sure node is installed [node installation](http://nodejs.org/download/)
2. Clone this repo ```git clone https://github.com/openfin/grrd.git```
3. cd into the cloned project ```cd grrd```
4. Install the npm dependencies ```npm install```
5. Install the bower dependencies ```bower install```
6. Start the grunt process ```grunt serve```, after which your browser should automatically open

## Q external data source
An example QGridBehavior can be enabled by editing the index.html found within the dev environment.
1. Make sure q 32 bit free version is installed [Q free version](http://kx.com/software-download.php)
2. Startup either bigtable.q ```q bigtable.q``` or sorttable.q ```q sorttable.q```
3. Make sure grunt serve is running
4. Edit the file examples/dev/index.html
    1. Comment out the line ```grid.setBehavior(new InMemoryGridBehavior());```
    2. Uncomment the line ```//grid.setBehavior(new QGridBehaviour('ws://localhost:5000/'));``` 
5. The grunt serve process should automatically refresh your web browser with the q driven grid

## Custom Scrollbars
The OpenFin Grid utilizes a custom scrollbar component so as to not be limited to tables of 33MM pixels in width or height.   In addition to the custom scrollbar, The OpenFin Grid utilizes row and column cell scrolling, not pixel scrolling.  This has many benefits that become apparent after time.

## Road Map 
1. Test suite for all components and upstream dependency projects
2. Continued bug-fixing, refactoring, documentation and cleanup of the existing code base
3. Delegation of cell editing through GridBehavior / CellRendering objects
4. GridBehaviors for other data sources
5. Column reordering/resizing/autosizing
6. Hover event support
7. Tooltip support 
8. Layer abstraction

## Feature List
* High performant canvas based
* Arbitrary row/col sizes
* Data per cell can be anything (text, numerical, nested arrays, etc.)
* Shape/size in both pixel and row/column count can change dynamically
* Infinite scrolling row/col through external high performant data sources (see Q examples)
* Copy to paste buffer selected cells (work in progress...)
* Multi-rectangle based selection model
* Mouse driven dragging selections
* Shift/control selection augmentation
* Fast arrow key navigation
* Non-linear accelerated vertical key navigation
* Custom scrollbar implementation for infinite scroll of large data sets
* Cell based scrolling (not pixel) 
* Pluggable behavior based eventing
* In place editing mechanism using html5 overlayed components
* Simple Q-based GridBehavior example provided with 2 q scripts. 100MM example, and 1MM sortable example
* Simple in memory based GridBehavior example provided
* Easily customizable and extensible cell rendering
* Npm/grunt-based full featured dev environment
* ...
