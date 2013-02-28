Responsive Columns
==================

A simple framework to work with dynamic and responsive websites which need more than 3 or 4 breakpoints


## Setup a column framework which allows for finer control
* 1 column === 100px
* 2 columns === 200px
* etc. etc.

```sass
@mixin breakpoint($columns) {

    @if $columns == 1 {
        @media (max-width: 100px) { @content; }
    }
    @else if $columns == 2 {
        @media (min-width: 101px) and (max-width: 200px) { @content; }
    }
    @else if $columns == 3 {
        @media (min-width: 201px) and (max-width: 300px) { @content; }
    }
    @else if $columns == extra-large {
        @media (min-width: 301px) { @content; }
    }
}
```

## Overkill?
* This may look like overkill, but you don't HAVE to use all of them, just the ones you need (just like using a grid
layout)
* This methodology will give you the ability get finer control of your responsive websites in a way that people are 
able to understand in a easy way


## You can use EM's or percent aswell
Em's
```sass
@mixin breakpoint($columns) {

    @if $columns == 1 {
        @media (max-width: 100em) { @content; }
    }
    @else if $columns == 2 {
        @media (min-width: 101em) and (max-width: 200em) { @content; }
    }
    @else if $columns == 3 {
        @media (min-width: 201em) and (max-width: 300em) { @content; }
    }
    @else if $columns == extra-large {
        @media (min-width: 301em) { @content; }
    }
}
```

Percent
```sass
@mixin breakpoint($columns) {

    @if $columns == 1 {
        @media (max-width: 10%) { @content; }
    }
    @else if $columns == 2 {
        @media (min-width: 10.1%) and (max-width: 20%) { @content; }
    }
    @else if $columns == 3 {
        @media (min-width: 20.1%) and (max-width: 30%) { @content; }
    }
    @else if $columns == extra-large {
        @media (min-width: 30.1%) { @content; }
    }
}
```


