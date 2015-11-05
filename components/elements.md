# Elements

Elements are things inside your component.

![](https://raw.githubusercontent.com/arxpoetica/gs-css-rules/master/img/component-elements.png)

## Naming elements

Each component may have elements. They should have classes that are only **one word**.

```scss
.search-form {
	.field { /* ... */ }
	.action { /* ... */ }
}
```

## Multiple words

For those that need two or more words, concatenate them without dashes or underscores.

```scss
.profile-box {
	.firstname { /* ... */ }
	.lastname { /* ... */ }
	.dansbrain { /* ... */ }
}
```

## Classnames or tag selectors?

Classnames are more descriptive, provide greater specificity, and may provide better performance. However, when generic targeting is needed, don't be afraid to target tag selectors. Such a thing is just fine.

```scss
.ians-cubicle {
	h3      { /* ✓ target all h3 tags */ }
	.name   { /* ✓ be specific */ }
	h3.name { /* ✗ avoid */ }
}
```

## Greater specificity

At times, you might not want a selector to bleed through to any nested elements or components. Use the `>` child selector to tightly control descendants.

```scss
.article-card {
	.title    { /* specific */ }
	> .author { /* ✓ very specific */ }
}
```

Not all elements should always look the same. Variants can help. [Continue →](variants.md)
