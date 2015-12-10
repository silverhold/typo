# typo-helper
Sass helper for managing typography components on projects

## Getting Started
to be defined

## Usage

### font-face
To simplify the font import with `@font-face` a mixin is available, you can use it as below:

```
@include font-face($name, $path, $weight: normal, $style: normal, $exts: eot woff2 woff ttf svg);
```

The font-family name and path are required, but the weight, the style and the extentions to import into the font-face have those default values.


#### Example
```
@include font-face('my font', '../fonts/myfont', '400', italic, ttf);
```
