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
* Sure, this may look like overkill, but you don't HAVE to use all of them, just the ones you need (just like using a grid
layout)
* This methodology gives you finer control of your responsive websites in a way that you can understand


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


# Full Code Example:
```sass
@mixin breakpoint($columns) {

    @if $columns == 1 {
        @media (max-width: 100px) { @content; }
    }
    @else if $columns == 2 {
        @media (max-width: 200px) { @content; }
    }
    @else if $columns == 3 {
        @media (max-width: 300px) { @content; }
    }
    @else if $columns == 4 {
        @media (max-width: 400px) { @content; }
    }
    @else if $columns == 5 {
        @media (max-width: 500px) { @content; }
    }
    @else if $columns == 6 {
        @media (max-width: 600px) { @content; }
    }
    @else if $columns == 7 {
        @media (max-width: 700px) { @content; }
    }
    @else if $columns == 8 {
        @media (max-width: 800px) { @content; }
    }
    @else if $columns == 9 {
        @media (max-width: 900px) { @content; }
    }
    @else if $columns == 10 {
        @media (max-width: 1000px) { @content; }
    }
    @else if $columns == 11 {
        @media (max-width: 1100px) { @content; }
    }
    @else if $columns == 12 {
        @media (max-width: 1200px) { @content; }
    }
    @else if $columns == 13 {
        @media (max-width: 1300px) { @content; }
    }
    @else if $columns == 14 {
        @media (max-width: 1400px) { @content; }
    }
    @else if $columns == 15 {
        @media (max-width: 1500px) { @content; }
    }
    @else if $columns == 16 {
        @media (min-width: 1501px) { @content; }
    }
}

article {
    background: #BBB;
    float: left;
    height: 400px;
    padding: 20px;
    width: 65%;

    @include breakpoint(9) {
        width: 75%;
    }

    @include breakpoint(7) {
        width: 50%;
    }

    @include breakpoint(4) {
        width: 100%;
    }
}
```
