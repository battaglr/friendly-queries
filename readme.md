# Medly queries

Human-friendly media queries in Sass.

## Overview

A set of mixins that attempts to make working with media queries a bit easier
by using memorable names to define them.

## Installation

```sh
$ bower install medly-queries
```

*Requires Sass ^3.4.0.*

## Usage

1. Basic usage:

  ```scss
  selector {
    property: value;

    @include viewport-above(narrow) {
      property: value;
    }
  }
  ```

  *Output:*

  ```css
  selector {
    property: value;
  }

  @media only screen and (min-width: 40em) {
    selector {
      property: value;
    }
  }
  ```

2. Modify the direction:

  ```scss
  selector {
    property: value;

    @include device-below(large, vertical) {
      property: value;
    }
  }
  ```

  *Output:*

  ```css
  selector {
    property: value;
  }

  @media only screen and (min-device-height: 64em) {
    selector {
      property: value;
    }
  }
  ```

3. Nesting:

  ```scss
  selector {
    property: value;

    @include device-below(small, vertical) {
      property: value;

      @include orientation(portrait) {
        property: value;
      }
    }
  }
  ```

  *Output:*

  ```css
  selector {
    property: value;
  }

  @media only screen and (min-height: 25em) {
    selector {
      property: value;
    }
  }

  @media only screen and (min-height: 25em) and (orientation: portrait) {
    selector {
      property: value;
    }
  }
  ```

### Mixins

Available mixins:

1. `density-above()`
2. `density-below()`
3. `density-between()`
4. `device-above()`
5. `device-below()`
6. `device-between()`
7. `orientation()`
8. `print()`
9. `viewport-above()`
10. `viewport-below()`
11. `viewport-between()`

### Conditions

Define the different conditions for the media queries inside the
`$media-conditions` map.

**Note**: `horizontal` and `vertical` keys are `0` by default, to help you
remember that the only thing that should determinate those dimensions is your
content.

## License

Released under the [MIT license](license.txt).
