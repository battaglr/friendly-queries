# Breakpoint

Human-friendly breakpoints with Sass.

## What is this?

A small set of mixins that attempts to make working with media queries a bit
easier by using memorable names to define each breakpoint.

If you're looking for an extensive solution, this isn't for you. We keep things
simple in here.

## How do I use it?

There are 3 different mixins to choose from:

1. `breakpoint-below()`
2. `breakpoint-above()`
3. `breakpoint-between()`

And 7 variables to define the viewport width:

1. `$viewport-narrowest`
2. `$viewport-narrower`
3. `$viewport-narrow`
4. `$viewport-medium`
5. `$viewport-wide`
6. `$viewport-wider`
7. `$viewport-widest`

If you're familiar with Sass, the usage is very straight forward:

```scss
selector {
  property: value;

  @include breakpoint-above($viewport-narrow) {
    another-property: value;
  }
}
```

## Let content determine your breakpoints!

You will notice that the value of all variables is `0`. That's to ~~annoy~~
help you remember that devices do not matter, your content does. Let it define
your breakpoints.

## License

I don't care about legal stuff nor attribution. Do whatever you want with this,
it's public domain.
