# HTML Codin’ Style

This document only defines style and formatting rules for writing HTML documents.
It’s based on personal preferences and doesn’t pretend to be the “one and only”
way of doing it.

## Whitespace

- Use Unix newline character: `LF`.
- Use two spaces per indentation level.
- Remove all trailing whitespace.
- Always end files with a newline.
- Use only one blank line as a separator.

_Psst, you may want to check my [presentation about whitespace]
(http://speakerdeck.com/battaglr/why-you-should-care-about-whitespace)_.

## Elements

- Use lowercase for opening and closing tags.
- Use an additional level of indentation for each nested element.
- Always use closing tags.
- Always include a space followed by a trailing slash in self-closing elements.

```html
<div class="panel">
  <div class="panel__heading">
    <h2 class="panel__title"> ... </h2>
  </div>
  <div class="panel__content">
    <p> ... </p>
    <figure>
      <img src="photograph.jpg" />
      <figcaption>
        ... <a href="foob.ar"> ... </a>
      </figcaption>
    </figure>
  </div>
</div>
```

## Attributes

Use lowercase for attribute names.

```html
<!-- DON'T -->
<input data-fooBar="value" />

<!-- DO -->
<input data-foo-bar="value" />
```

Use valueless boolean attributes.

```html
<!-- DON'T -->
<input type="checkbox" checked="checked" />

<!-- DO -->
<input type="checkbox" checked />
```

Use double quotes on attribute values.

```html
<!-- DON'T -->
<input type='text' />
<input type=text />

<!-- DO -->
<input type="text" />
```

Elements with multiple attributes should be arranged across multiple lines:

- Place the first attribute in the same line of the opening tag.
- Place the following attributes in a newline using one extra space
  for indentation.

```html
<div class="panel panel--collapsible"
 id="attributes"
 data-component="collapsible-panel"
 data-animation="slide-down">
  <div class="panel__heading"> ... </div>
  <div class="panel__content"> ... </div>
</div>
```

### Attribute order

Write attributes in the following order:

1. Class: `class`.
2. Data: `data-*`.
3. Id: `id`.
4. Name: `name`.
5. Everything else.

````html
<input class="value" data-custom="value" id="value" name="value" type="value" />
````

## License

Do whatever you want with this, it’s public domain.
