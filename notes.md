
rem instead of pixels for making media queries easier to write
html (root) set to font-size 10px 
1 rem is exactly 10 pixels
10/16 = 0625 we started with 16px
62.5%
for example if i wanted 20px root font size => 10/20 = 0.5 = 50%

BEM - __ for block -- for things u can use all over webbsite

## SASS
sass source code => sass compiler => compiled css code
sass is a preprocessor an extension to css that makes it more elegant

### sass gives us variables
### nesting to nest selectors inside of one another
### partials and imports to write css in different files
### mixins to write reusable pieces of css code 
### functions similar to mixins but they produce a value that can be used later
### extends to make different selectors inherit declarations
### control directives for writing complex code using coditional and loops

## sass syntax
.nav {
    list-style: none
    float: left

    & li 
        display: inline.block
}

## scss syntax 
.nav {
    list-style: none;
    float: left;

    & li {
        display: inline.block;
    }
}

in sass you can comment like // 
define variables with $

.navigation {
  list-style: none;
  
  li {
    display: inline-block;
    margin-left: 30px;
    
    &:first-child {
    margin: 0;
    }
  }
}
//.navigation-li:first-child

### compiling sass
in package.json:

 "scripts": {
    "compile:sass": "node-sass sass/main.scss css/style.css -w"
  }
in terminal => npm run compile:sass
the -w works so that the css file i autoupdated and render in browser is updated.

_main.scss only have imports

## Layout
### Grid
use max-width for window to adapt to screen
margin: 0 auto => centers the grid

&:not(:last-child)
in sass we put the margin-bottom to all rows except the last one

calc() funtion in sass where you can do operations with multiple units (rem, px, em etc..)

ATTRIBUTE:
[class^="col"] = where all class attributes start with "col" 
* = contain
$ = any class that ends

