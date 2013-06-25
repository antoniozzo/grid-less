# Grid-Less

A very simple grid system with bubbling media queries.
With Grid-Less you can create perfect responsive layout in just a few lines of code.

## How to use

Just import grid.pack.less in you less file:

<pre><code>import 'grid.pack.less';
</code></pre>

This is how you create 3 responsive layouts with Grid-Less and media queries:

<pre><code>@max-width: 960px; // A 960 grid

#wrapper
{
	.container; // Our wrapper is a container
}

#header
{
	.col; // Full width column on a desktop
}

#content
{
	.col(75%); // A 3/4 column on a desktop
	
	@media @tablet-landscape { .col(50%); }  // A 1/2 column on a tablet in landscape
	@media @mobile-landscape { .col; }  // A full width column on a mobile in landscape
}

#sidebar
{
	.col(25%); // A 1/4 column on a desktop
	
	@media @tablet-landscape { .col(50%); }  // A 1/2 column on a tablet in landscape
	@media @mobile-landscape { .col; }  // A full width column on a mobile in landscape
}

#footer
{
	.col; // Full width column on a desktop
}
</code></pre>

## Available variables

You can customize these variables:

<pre><code>
@min-width: 320px; // Min-width of a container
@max-width: 1140px; // Max-width of a container
@gutter: 30px; // Gutter width of columns
</code></pre>

Here is the available media queries (Must be used in this order):

<pre><code>
@desktop: ~'only screen and (max-width : 1824px)';
@desktop-small: ~'only screen and (max-width : 1224px)';
@tablet-landscape: ~'only screen and (max-width : 1024px)';
@tablet: ~'only screen and (max-width : 980px)';
@mobile-landscape: ~'only screen and (max-width : 767px)';
@mobile: ~'only screen and (max-width : 321px)';
@retina: ~'only screen and (-webkit-min-pixel-ratio : 1.5), only screen and (min-pixel-ratio : 1.5)';
</code></pre>

## Baseline Grid (Documentation coming soon!)