The Masonry Layout kind is a port of the [Vanilla Masonry](http://vanilla-masonry.desandro.com/index.html) from David DeSandro. It provides dynamic layout of a container's contents based on the sizes of the contents. It does its best to fit the contents as if they were bricks being arranged into a wall, hence the name Masonry.

Included is a LayoutKind called `com.Pre101.MasonryLayout` and a kind called `com.Pre101.Masonry`. Use LayoutKind when you wish to apply the Masonry style to an existing kind. You may use the Masonry kind when you don't care about the base kind of the container.

Example Usage
-------------

	enyo.kind({
		name: "SingleColumn",
		kind: "com.Pre101.Masonry",
		components: []
	});
	
or

	enyo.kind({
		name: "LayoutExample",
		layoutKind: "com.Pre101.MasonryLayout",
		components: []
	});

Parameters
----------

Masonry supports several parameters that can be set. In order to pass parameters to the Layout you must set them on the container. The following parameters are supported:

* `columnWidth`: Width in pixels of one column of your grid. If no columnWidth is specified, Masonry uses the width of the first item element. Recommended if your layout has item elements that have multiple-column widths. You may set this to a function that receives the width of the container as a parameter and returns the width in pixels.

* `gutterWidth`: Additional spacing between columns, in pixels.

* `isFitWidth`: (Boolean) If enabled, container will be resized to the nearest column width multiple that fits within the parent object's width.

* `isRTL`: (Boolean) Enables right-to-left layout.

For more information, please see the Vanilla Masonry site.

Demo: See [SingleColumn demo](http://dynaptic.com/enyo/Masonry/examples/SingleColumn.html)