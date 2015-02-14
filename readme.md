# HTML Codin’ Style

This document only defines style and formatting rules for writing HTML documents.
It’s based on personal preferences and doesn’t pretend to be the “one and only”
way of doing it.

## Whitespace

+ Use Unix newline character: `LF`.
+ Use two spaces per indentation level.
+ Remove all trailing whitespace.
+ Always end files with a newline.
+ Use only one blank line as a separator.

_Psst, you may want to check my [presentation about whitespace]
(http://speakerdeck.com/battaglr/why-you-should-care-about-whitespace)_.

## Elements

+ Use lowercase for opening and closing tags.
+ Use an additional level of indentation for each nested element.
+ Always use closing tags.
+ Always include a space followed by a trailing slash in self-closing elements.

```html
<div class="panel">
  <div class="panel__heading">
    <h2 class="panel__heading__title">The title</h2>
  </div>
  <div class="panel__content">
    <p>Some content.</p>
    <figure>
      <img src="photograph.jpg" />
      <figcaption>A caption with a <a href="foob.ar">link</a>.</figcaption>
    </figure>
  </div>
</div>
```

## Attributes

Use lowercase for attribute names.

```html
<input data-foo-bar="value" />
<input data-fooBar="value" /> <!-- Don't! -->
```

Use valueless boolean attributes.

```html
<input type="checkbox" checked />
<input type="checkbox" checked="checked" /> <!-- Don't! -->
```

Use double quotes on attribute values.

```html
<input type="text" />
<input type='text' /> <!-- Don't! -->
<input type=text /> <!-- Don't! -->
```

Elements with multiple attributes should be arranged across multiple lines:

+ Place the first attribute in the same line of the opening tag.
+ Place the following attributes in a newline using one extra space
  for indentation.

```html
<div class="panel panel--collapsible"
 id="attributes"
 data-component="collapsible-panel"
 data-animation="slide-down">
  <div class="panel__heading"></div>
  <div class="panel__content"></div>
</div>
```

### Attribute order

Write attributes in the following order:

1. Class: `class`.
2. Id: `id`.
3. Data: `data-*`.
4. Name: `name`.
5. Everything else.

````html
<input class="value" id="value" data-custom="value" name="value" type="value" />
````

## License

Do whatever you want with this, it’s public domain.
