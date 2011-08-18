# Vendor Prefix Mixins

Save your fingers from excess typing by using these handy mixins for use with LessCSS. 
Easily add all the required vendor prefixes when using new fangled CSS properties.

## Supported properties

 + border-radius
 + box-shadow
 + gradients
 + rgba
 + rotate
 + scale
 + translate
 + skew
 + transition
 + background-size
 + box-sizing
 + columns
 
## Usage

Ensure that the mixins lessCSS file has been imported

    @import "mixins.less";

Then use any of the mixins within your own declarations

### Input

    header {
        .border-radius(6px);
        .box-shadow(0px, 0px, 4px, 2px, #333);
        .rotate(7.5deg);
        
        a:hover {
            color: red;
            .transition(color);
        }
    }

### Output

    header {
        -moz-border-radius: 6px;
        -webkit-border-radius: 6px;
        border-radius: 6px;
        -moz-background-clip: padding;
        -webkit-background-clip: padding-box;
        background-clip: padding-box;
        -moz-box-shadow: 0px 0px 4px 2px #333333;
        -webkit-box-shadow: 0px 0px 4px 2px #333333;
        box-shadow: 0px 0px 4px 2px #333333;
        -moz-transform: rotate(7.5deg);
        -o-transform: rotate(7.5deg);
        -webkit-transform: rotate(7.5deg);
        -ms-transform: rotate(7.5deg);
        transform: rotate(7.5deg);
    }
    header a:hover {
        color: red;
        -webkit-transition: color 0.5s linear 0s;
        -moz-transition: color 0.5s linear 0s;
        -ms-transition: color 0.5s linear 0s;
        -o-transition: color 0.5s linear 0s;
        transition: color 0.5s linear 0s;
    }
