# Planning Center Minions

A [minions.css](https://github.com/chantastic/minions.css) extensions for [Planning Center](https://planning.center/) app colors.

Supports `background-color`, `border-color`, `color`, and `fill` properties.

[example](http://chantastic.github.io/planningcenter-minions.css)

## Usage

`planningcenter-minions.css` is a context-provider. In the majority case, context is provided by the host application. However, cross-applicatin modals need a way to cascade styles where host context is unavailable (iFrame).

In minions, these context providers look like variables: `<body class="appcolor=accounts">`.

The elements that observe these contexts are written like this: `<div class="c-appcolor">`. This element's color would be the application color.

### Example

```html
<body class="appcolor=accounts">
  <div><!-- modal-like thing -->
    <header class="gc-appcolor c-white">
      Edit a Person
    </header>

    <div>
      <p>Contentz.</p>
    </div>

    <footer>
      <button
        class="bc-appcolor c-appcolor gc-transparent"
        type="button"
        value="Create"
      />

      <input
        class="gc-appcolor c-white"
        type="submit"
        value="Create"
      />
    </footer>
  </div>
</body>
```

## Installation

The [main css](./planningcenter-minions.css) file is in the root of this project. Copy/paste 

### NPM

Install the package.

```bash
npm i -D planningcenter-minions.css
```

Add it to your build pipeline. I'll assume you know how to do that. Here's what it looks like using Webpakc/css-laoder:

```js
import "planningcenter-minions"
```

### link tag

Obviously you can include this using a link-tag.

```html
<link rel="stylesheet" href="./path/to/planningcenter-minions.css" />
```