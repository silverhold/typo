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

### font-family
You can set a map with a bunch of couple key, value for generating as many helper classes for setting a font-family to a selector.
The default value for the `$font-family__list` variable is:
```
$font-family__list: (
    'serif': 'Times New Roman, Bodoni, Garamond, Minion Web, ITC Stone Serif, MS Georgia, Bitstream Cyberbit',
    'sans-serif': 'MS Trebuchet, ITC Avant Garde Gothic, MS Arial, MS Verdana, Univers, Futura, ITC Stone Sans, Gill Sans, Akzidenz Grotesk, Helvetica',
    'cursive': 'Caflisch Script, Adobe Poetica, Sanvito, Ex Ponto, Snell Roundhand, Zapf-Chancery',
    'fantasy': 'Alpha Geometrique, Critter, Cottonwood, FB Reactor, Studz',
    'monospace': 'Courier, MS Courier New, Prestige, Everson Mono',
) !default;
```
This will create a class `.font-family--serif` with for rule `font-family: Times New Roman, Bodoni, Garamond, Minion Web, ITC Stone Serif, MS Georgia, Bitstream Cyberbit` and etc for each occurence of the `$font-family__list` map.

If you want to change the prefix of the generated class you can by resetting the variable `$font-family__selector-prefix` set as default as below:
```
$font-family__selector-prefix: 'font-family--' !default;
```

There is also a class generated for the `inherit` value of the `font-family` property. The `.font-family--inherit` is generated by default but you can turn it of by switching to false the variable `$font-family__include--inherit`.

If you want to extend a selector to one of the helper class generated you can use the mixin `font-family--extend($name)`, as shown below.
```
.selector {
    @include font-family--extend(monospace);
}
```

You can avoid typo-helper to generate any helper font-family helper class by switching to false the `$font-family` variable.

### font-style
Font style classes are generated with the variable list `$font-style__list` that will generate class with all the values possible for the rule `font-style` (normal, italic, oblique). You can edit the list to avoid one or several helper class. Default value of the `$font-style__list` variable.
```
$font-style__list: (normal, italic, oblique) !default;
```

You can also generate class for the inherit value by setting to `true` the `$font-style__include--inherit` variable.
If you don't want to generate any helper class for font-style property you can set the `$font-style` variable to `false`.

If you want to extend a selector to one of the helper class generated you can use the mixin `font-style--extend($name)`, as shown below.
```
.selector {
    @include font-style--extend(italic);
}
```

### font-variant
Font variant classes are generated with the variable list `$font-variant__list` that will generate class with all the values possible for the rule `font-variant` (normal, small-caps). You can edit the list to avoid one or several helper class. Default value of the `$font-variant__list` variable.
```
$font-variant__list: (normal, small-caps) !default;
```

You can also generate class for the inherit value by setting to `true` the `$font-variant__include--inherit` variable.
If you don't want to generate any helper class for font-variant property you can set the `$font-variant` variable to `false`.

If you want to extend a selector to one of the helper class generated you can use the mixin `font-variant--extend($name)`, as shown below.
```
.selector {
    @include font-variant--extend(italic);
}
```

### font-weight
You can set a map with a bunch of couple key, value for generating as many helper classes for setting a font-weight to a selector.
The default value for the `$font-weight__list` variable is:
```
$font-weight__list: (
    'light': 100,
    'normal': 400,
    'bold': 600,
) !default;
```
This will create a class `.font-weight--bold` with for rule `font-weight: 600` and etc for each occurence of the `$font-weight__list` map.

If you want to change the prefix of the generated class you can by resetting the variable `$font-weight__selector-prefix` set as default as below:
```
$font-weight__selector-prefix: 'font-weight--' !default;
```

There is also a class generated for the `inherit`, `lighter` and `bolder` value of the `font-weight` property. The `.font-weight--inherit`, `.font-weight--lighter` or `.font-weight--bolder` are generated by default but you can turn it of by switching to false the variables `$font-weight__include--inherit`, `$font-weight__include--lighter` or `$font-weight__include--bolder`.

If you want to extend a selector to one of the helper class generated you can use the mixin `font-weight--extend($name)`, as shown below.
```
.selector {
    @include font-weight--extend(light);
}
```

You can avoid typo-helper to generate any helper font-weight helper class by switching to false the `$font-weight` variable.

### font-size
You can set a map with a bunch of couple key, value for generating as many helper classes for setting a font-size to a selector.
The default value for the `$font-size__list` variable is:
```
$font-size__list: (
    'small': 14px,
    'normal': 16px,
    'large': 18px,
) !default;
```
This will create a class `.font-size--serif` with for rule `font-size: Times New Roman, Bodoni, Garamond, Minion Web, ITC Stone Serif, MS Georgia, Bitstream Cyberbit` and etc for each occurence of the `$font-size__list` map.

If you want to change the prefix of the generated class you can by resetting the variable `$font-size__selector-prefix` set as default as below:
```
$font-size__selector-prefix: 'font-size--' !default;
```

There is also a class generated for the `inherit` value of the `font-size` property. The `.font-size--inherit` is generated by default but you can turn it of by switching to false the variable `$font-size__include--inherit`.

If you want to extend a selector to one of the helper class generated you can use the mixin `font-size--extend($name)`, as shown below.
```
.selector {
    @include font-size--extend(small);
}
```

You can avoid typo-helper to generate any helper font-size helper class by switching to false the `$font-size` variable.

### text-decoration
Font style classes are generated with the variable list `$text-decoration__list` that will generate class with all the values possible for the rule `text-decoration` (none, underline, overline, line-through). You can edit the list to avoid one or several helper class. Default value of the `$text-decoration__list` variable.
```
$text-decoration__list: (none, underline, overline, line-through) !default;
```

You can also generate class for the inherit value by setting to `true` the `$text-decoration__include--inherit` variable.
If you don't want to generate any helper class for text-decoration property you can set the `$text-decoration` variable to `false`.

If you want to extend a selector to one of the helper class generated you can use the mixin `text-decoration--extend($name)`, as shown below.
```
.selector {
    @include text-decoration--extend(underline);
}
```

### text-transform
Font style classes are generated with the variable list `$text-transform__list` that will generate class with all the values possible for the rule `text-transform` (capitalize, uppercase, lowercase, none). You can edit the list to avoid one or several helper class. Default value of the `$text-transform__list` variable.
```
$text-transform__list: (capitalize, uppercase, lowercase, none) !default;
```

You can also generate class for the inherit value by setting to `true` the `$text-transform__include--inherit` variable.
If you don't want to generate any helper class for text-transform property you can set the `$text-transform` variable to `false`.

If you want to extend a selector to one of the helper class generated you can use the mixin `text-transform--extend($name)`, as shown below.
```
.selector {
    @include text-transform--extend(uppercase);
}
```

### text-align
Font style classes are generated with the variable list `$text-align__list` that will generate class with all the values possible for the rule `text-align` (left, right, center, justify). You can edit the list to avoid one or several helper class. Default value of the `$text-align__list` variable.
```
$text-align__list: (left, right, center, justify) !default;
```

You can also generate class for the inherit value by setting to `true` the `$text-align__include--inherit` variable.
If you don't want to generate any helper class for text-align property you can set the `$text-align` variable to `false`.

If you want to extend a selector to one of the helper class generated you can use the mixin `text-align--extend($name)`, as shown below.
```
.selector {
    @include text-align--extend(left);
}
```
