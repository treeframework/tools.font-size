# font-size

Create a fully formed type style (sizing and vertical rhythm) by passing in a
single value.

## Dependencies

The `font-size` module depends on one other module:

* [settings.defaults](https://github.com/treeframework/settings.defaults)

If you install the `font-size` module using Bower or npm, you will get these 
dependencies at the same time. If not using Bower or npm, please be sure  to 
install and `@import` these dependencies in the  relevant way.

## Installation

You can install the `font-size` module via Bower, npm, or copy and paste.

### Install using Bower:

```sh
$ bower install tree-font-size --save
```

Once installed, `@import` into your project in its Tools layer:

```scss
@import "bower_components/tree-font-size/tools.font-size";
```

### Install using npm:

```sh
$ npm install tree-font-size --save
```

### Install via file download

The least recommended option for installation is to simply download
`_tools.font-size.scss` into your project and `@import` it into your 
project in its Tools layer.

## Usage

Basic usage of the `font-size` module:

```scss
.foo {
    @include tree-font-size(12px);
}
```

This will generate a rem-based font-size with its pixel fallback, as well as
a unitless line-height which will place the element on your baseline, e.g.:

```css
.foo {
    font-size: 12px;
    font-size: 0.75rem;
    line-height: 2;
}
```

If you do not want to generate you a line-height automatically, you simply pass 
in your own as a second parameter:

```scss
.foo {
    @include tree-font-size(12px, 1.5);
}
```

This will yield:

```css
.foo {
    font-size: 12px;
    font-size: 0.75rem;
    line-height: 1.5;
}
```

This parameter can be any integer, ‘inherit’, or ‘normal’. If you don't want
a line-height at all, pass in a second parameter of ‘none’ or ‘false’:

```scss
.foo {
    @include tree-font-size(12px, none);
}
```

This will yield:

```css
.foo {
    font-size: 12px;
    font-size: 0.75rem;
}
```

## Credits

* **[inuitcss](https://github.com/inuitcss)** Powerful, Sass-based, OOCSS
framework designed with scalability and performance in mind.
