# CSS

## Syntax

- When grouping selectors, keep individual selectors to a single line
- Include one space before the opening brace of declaration blocks for legibility
- Place closing braces of declaration blocks on a new line
- Include one space after `:` for each declaration
- Each declaration should appear on its own line for more accurate error reporting
- End all declarations with a semi-colon, including the last in order to avoid errors
- Comma-separated property values should include a space after each comma
- In order to differentiate between multiple (non-hex) color values from multiple property values, do not use spaces after commas when using `rgb()`, `rgba()`, `hsl()`, `hsla()` or `rect()` values
- Prefix property values or color parameters with a leading zero (e.g., 0.5 instead of .5 and -0.5px instead of -.5px)
- Lowercase all hex values, e.g., `#fff`
- Use shorthand hex values when possible `#fff` instead of `#ffffff`
- Where quotes are required, use double-quotes `"` to stay consistent across CSS and HTML
- Though not required in every instance, use double-quotes around attribute values in selectors to enforce consistency and avoid errors
- Do not specify units for zero values
- Separate each rule set with a single line

```css
/* Do: */
.container,
.container-secondary,
.container-input[type="text"] {
    background: rgba(0,0,0,0.5);
    box-shadow: 0 1px 3px #000, inset 0 0 6px #333;
    margin: 4px 0;
    text-shadow: 0 1px 3px #fff;
}

.wrap {
    width: 100%;
}
```

```css
/* Don't: */
.container,.container-secondary,.container-input[type=text]{
    background:rgba(0,0,0,.5);
    box-shadow:0px 1px 3px #000000,inset 0px 0px 6px #333333;
    margin:4px 0px;
    text-shadow:0px 1px 3px #fff;
}
.wrap{
    width:100%
}
```

## Declaration order

To maintain readability, make it easier to locate errors and for ease-of-maintenance, property declarations should be listed in alphabetical order.

## Single Declarations

In order to maintain consistency, single declarations should follow the same rules as multi-line declarations:

```css
/* Do */
.wrap {
    width: 50%;
}
```

```css
/* Don't */
.wrap { width: 50%; }
```

## Shorthand properties

To improve code efficiency and ease-of-maintenance, use shorthand properties whenever possible. However, there are certain instances where using shorthand becomes inefficient:

```css
/* Efficient */
margin-left: 6px;
```

```css
/* Less efficient */
margin: 0 0 0 6px;
```

## Naming conventions

- **All classnames are to be lowercase and use dashes when applicable.** Do not use underscore or camelCase.
- Shorthand is encouraged but to be used only sparingly and when reasonable. Example: ```.btn``` instead of ```.button```. Using shorthand that is not recognizable is not useful.
- Use meaningful names that are more about structure than presentation. An upload button may not forever exist as ```.orange-btn-upload```.
- Whenever possible, prefix classes using their closest parent or base class. Example ```.section-header```.

## Selectors

**Avoid using type selectors at all costs.** HTML elements are not always guaranteed to stay the same.

## Comments

More is better. Comments are best when they best describe why a declaration or block of declarations exist, what their function is, how they work, etc.

- Where applicable, comments should maintain a visual hierarchy
- Each comment should occupy it's own line
- Keep line-length to a maximum of 80 columns

Example:

```css
/* ---------- SECTION BLOCK COMMENT ---------- */

/* ----- Subsection block comment ----- */

/*
This is a long comment used to describe lorem ipsum dolor sit amet, consectetur
adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna
aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi
ut aliquip ex ea commodo consequat.
*/

/* Basic comment */
```

## Organization

- Organize sections of code by component.
- Develop a consistent commenting hierarchy.
- Use consistent white space to your advantage when separating sections of code for scanning larger documents.
- When using multiple CSS files, break them down by component instead of page. Pages can be rearranged and components moved.

## Bad Habits to Avoid

- **Inline-styling is the enemy.** Unless in the rare situation when it is required, inline-styling is absolutely not acceptable.
- **Negative margins.** There are times when they are a good idea. These times are few and far between, it's best to avoid using them.
- **Color names vs. hex values.** You should not use color names at the expense of ```#hex```, ```rgb()```, ```rgba()```, ```hsl()``` or ```hsla()```.



