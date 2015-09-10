# SCSS

## Chaining

If you need to chain selectors, do not use more than three. This will help to put a limit on specifity which can be bad unless absolutely neccessary.

Example:

```scss
// Acceptable
.parent {
    ...
}

.parent .child {
    ...
}

.parent .child .grandchild {
    ...
}
```

```scss
// Not acceptable
.one > .two > .three > .four {
    ...
}
```

## Nesting

Just as with chaining, avoid nesting more than 3 levels deep at all costs. This again will limit specifity and avoid the code being unreadable and unsearchable.

When nesting, each nested item should be separated from it's parent and or siblings by a single line.

Example:

```scss
// Do
.parent {

    .sibling-heading {
        ...
    }

    .sibling-content {
        ...
    }

}
```

```scss
// Don't
.parent {
    .sibling-heading {
        ...
    }
    .sibling-content {
        ...
    }
}
```

## Vendor prefixes

Do not use them unless absolutely neccessary. There are many mixins at your disposal in order to avoid having to.

## Mixins vs. Placeholders

Rule of thumb: Use mixins only when a variable needs to be passed. If it doesn't require a variable, placeholders are the way to go. First, you can’t use variables in a placeholder. Actually you can but you cannot pass variables to your placeholders so you can’t generate context-specific CSS like you would do with a mixin. Second, the way Sass handles mixins makes them very inconvenient when you don’t use them with contextual variables. To put it simply: Sass will duplicate the output of the mixin every time you use it, resulting not only in duplicated CSS but also a bigger stylesheet.

## ```@extend``` & ```@include```

- Always place ```@extend``` statements on the first lines of a declaration block.
- Whenever possible, group any ```@extend``` and/or ```include``` statements at the top of the declaration block, with any ensuing simple declarations separated by a single line:

```scss
// Do
.example {
    @extend %placeholder;
    @include mixin(var);
    
    height: 100%;
    width: 100%;
}
```

```scss
// Don't
.example {
    @extend %placeholder;
    height: 100%;
    @include mixin(var);
    width: 100%;
}
```

## Importing SCSS Files

- When importing SCSS files, remember not to include leading underscores or file extensions
