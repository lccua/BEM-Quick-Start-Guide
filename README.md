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

```html
<form class="search-form">
```


## Element

### Explanation

- Integral part of a block that cannot be used separately.
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
<form class="search-form search-form--focused">
```

```html
<button class="search-form__button search-form__button--disabled">Search</button>
```

#### Key Value


```html
<form class="search-form search-form--theme--islands">
```

```html
<button class="search-form__button search-form__button--size--m">Search</button>
```
## :exclamation: **Important Notice** :exclamation:

A modifier can't be used alone 

#### Correct Example

```html
<form class="search-form search-form--theme--islands">
```

#### Incorrect Example

```html
<form class="search-form--theme--islands">
```

## Mix: Combining BEM Entities

The "Mix" method is a powerful BEM technique that involves applying multiple BEM entities (blocks and elements) to a single DOM node. This approach enables developers to merge behaviors and styles from different entities without code duplication, leading to the creation of new, semantically rich UI components from existing ones.

### Example of Mix Usage

Consider a scenario where we integrate the `search-form` block with the `header__search-form` element within the `header` block:

```html
<!-- Header Block -->
<div class="header">
    <!-- Mixing search-form block with header__search-form element -->
    <div class="search-form header__search-form"></div>
</div>
```


## Source
- https://en.bem.info/methodology/quick-start/#introduction

