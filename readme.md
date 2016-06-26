# Friendly queries

Human-friendly media queries for Sass.

## Overview

A set of mixins that attempts to make working with media queries a bit easier
by using memorable names to define them.

## Installation

Install it using [npm](https://npmjs.com):

```sh
npm install friendly-queries
```

## Usage

1. Basic usage:

  ```scss
  selector {
    property: value;

    @include viewport-above(small) {
      property: value;
    }
  }
  ```

  *Output:*

  ```css
  selector {
    property: value;
  }

  @media (min-width: 48em) {
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

  @media (min-device-height: 64em) {
    selector {
      property: value;
    }
  }
  ```

3. Nesting:

  ```scss
  selector {
    property: value;

    @include viewport-above(small) {
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

  @media (min-width: 48em) {
    selector {
      property: value;
    }
  }

  @media (min-width: 48em) and (orientation: portrait) {
    selector {
      property: value;
    }
  }
  ```

*You can see it in action on the
[test page](https://battaglr.github.io/friendly-queries/test/test.html).*

## Available mixins

- `density-above()`
- `density-below()`
- `density-between()`
- `device-above()`
- `device-below()`
- `device-between()`
- `orientation()`
- `print()`
- `viewport-above()`
- `viewport-below()`
- `viewport-between()`

## Conditions

Define the different conditions for the media queries inside the
`$friendly-queries` map.

## Contributing

Contributions are welcome! Please, read the
[contribution guidelines](contributing.md) first.

## License

Released under the [MIT license](license.txt).
