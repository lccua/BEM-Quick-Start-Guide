# BEM Quick Start Guide

BEM (Block, Element, Modifier) is a methodology designed for developing web interfaces with reusable components. Here's a quick guide to understanding the core concepts of BEM.

## Block

### Explanation

- Blocks are independent, reusable components, such as menus or buttons.
- They are identified by the `class` attribute in HTML.
- The block name should describe its purpose, not its appearance.

### Name Structure

```bash
block-name
```

### Example

```html
<div class="error"></div>
```

## Element

### Explanation

- Integral part of a block that cannot be used separately.
- Name structure: block-name__element-name.
- Elements can be nested but cannot be elements of other elements.


### Name Structure

```bash
block-name__element-name
```

### Example

```html
<input class="search-form__input">
```

## Modifier

### Explanation

- Defines appearance, state, or behavior of a block or element.
- Name structure: block-name_modifier-name or block-name__element-name--modifier-name.
- Types: Boolean (presence implies true) and Key-value (important value).

### Name Structure

#### Boolean

```bash
block-name__element-name--modifier-name
```

#### Key Value

```bash
block-name__element-name--modifier-name--modifier-value
```

### Example
#### Boolean
```html
<form class="search-form search-form_focused">
```

```html
<button class="search-form__button search-form__button_disabled">Search</button>
```

#### Key Value


```html
<form class="search-form search-form_theme_islands">
```

```html
<button class="search-form__button search-form__button_size_m">Search</button>
```

## Source
- https://en.bem.info/methodology/quick-start/#introduction

