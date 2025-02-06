# Tiny Grid
This is a lightweight CSS grid framework used to build responsive websites and applications. With just a size of 4KB minified (< 1KB gzipped), it is hard to find a smaller framework with the same possibilities.

## Quick Start
To use Tiny Grid in your project, download the CSS file `tiny-grid.min.css` located in the folder name css and include it in the head of you html page.

```html
<link rel="stylesheet" type="text/css" href="path/tiny-grid.min.css">
```

### The SCSS way
If you're using SCSS in you project, you could donwload the SCSS file instead. It is named `tiny-grid.scss` and located in the folder names scss. If you're doing it this way, you have more possibilities to customize the frameworks with your own breakpoints etc.

## Markup
Tiny Grid uses the same markup as Bootstrap's grid to make it easy to use for everyone. Example of the markup can be seen below:

```html
<div class="container">
  <div class="row">
    <div class="col-lg-6">This is a column</div>
    <div class="col-lg-6">This is another column</div>
  </div>
</div>
```

### Container
Container is a class to use to wrap all page content. The max-width is set by changing the `$grid-container-max-width` variable.

### Row
Rows should always wrap columns. This div contains negative margin to remove the padding from the outer columns.
```html
<div class="row">
  <!-- Columns goes here -->
</div>
```

### Columns
Breakpoint columns defines the width of the column in a certain breakpoint and up. Note that this frameworks uses `min-width` in the media queries.

The breakpoints could be defined in the `$grid-breakpoints` map. As default, Tiny Grid comes with the breakpoints `sm`, `md`, `lg` and `xl`.

As default, the grid system builds on a 12-column system. This could easily be changed by changing the `$grid-columns` variable to desired value.

#### Column construction
To construct a column, use the class `col-` followed by a breakpoint name and then a width (1 to 12).
```html
<div class="col-md-4"></div>
```
This example creates a column which will be 33.333% wide (4/12) in the md breakpoint and up.

#### Responsive columns
It is possible to use different column widths in different breakpoints. To do so, just add multiple `col-` classes.

```html
<div class="col-lg-4 col-md-6"></div>
```

#### Column offset
To add a offset to a column, use the `col-` class followed by breakpoint name, `-offset-` and then a width (1 to 12).
```html
<div class="col-lg-offset-2"></div>
```

### No-breakpoint depended columns
To add a column that is not depended by a breakpoint, just ignore the breakpoint name in the class construciton.


```html
<div class="col-6"></div>
```

## License
The MIT License (MIT)

