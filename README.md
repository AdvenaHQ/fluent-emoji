<image src='assets/images/banner.gif' alt='Microsoft Teams Animted emojis' />

# Fluent Emoji (Browser)

A simple library that provides standard Unicode emoji support across all platforms for Fluent Emoji. Fluent Emoji are a [collection of familiar, friendly, and modern emoji from Microsoft](https://github.com/microsoft/fluentui-emoji).

**This library is also offered as a drop-in replacement for [twemoji](https://github.com/twitter/twemoji)** which, due to recent changes at Twitter and the [deprecation of MaxCDN](https://github.com/twitter/twemoji#cdn-support), is no longer a viable option for many developers.

## Usage

### Content Delivery Network (CDN)

We recommend using [Advena's](https://github.com/AdvenaHQ) Fluent Emoji CDN for fast, simple emoji support.

Use the following script tag in the `<head>` tag of your HTML document(s):

```html
<script src="https://emoji.fluent-cdn.com/latest/fluentemoji.min.js" crossorigin="anonymous"></script>
```

This guarentees that you will always be using the latest version of the library.

If, instead, you'd like to include the latest version explicitly, you can add the following script tag instead:

```html
<script src="https://emoji.fluent-cdn.com/1.0.0/fluentemoji.min.js" integrity="sha256-G+vk3FHls/+I4Y8UV9jyCptUB8a4dnIXNeebVWc+Oo8= sha384-oAYDjisHrSixQ6gOZWkdOy/hd68sjETUF/FU+u2eoYbxBumADffLAxjhU8eweqKs sha512-ebCuNnS6S45CxCyNltbcf71VhjwZqHqOPe+RJncGHITkjgm5yIYQkJ8Z4u/F/mc5WndKF1YPfjZ7JFSRpekKrg==" crossorigin="anonymous"></script>
```

### API

## `fluentemoji.parse( ... )`

The `fluentemoji.parse()` is the main parsing utility, and takes a CSS selector. It will parse all text nodes within the provided element (including recursive child elements) and replace any emoji shortcodes with the appropriate emoji image.

```js
// Create example element
var div = document.createElement('div');
div.textContent = 'I ❤️ emoji!';
document.body.appendChild(div);

// Parse the div (will parse all elements on page)
twemoji.parse('div');
```

In the example above, the output would be:

```html
<div>I <img draggable="false" class="emoji" alt="❤️" src="https://emoji.fluent-cdn.com/1.0.0/100x100/2764-fe0f.png" /> emoji!</div>
```

By default, if no selector is provided, the `fluentemoji.parse()` method will parse all elements on the page. This is not necessarily recommended, as it can be a performance hit on larger pages.

You can target classnames, ids, and any other valid CSS selector. Here are some examples of valid selectors:

```js
twemoji.parse('div');
twemoji.parse('.my-class');
twemoji.parse('#my-id');
twemoji.parse('div > p');
twemoji.parse('div, p');
```

## Styling Fluent Emoji

Fluent Emoji are optimally styled using the following CSS class:

```css
.emoji {
    height: 1em;
    width: 1em;
    margin: 0 0.05em 0 0.1em;
    vertical-align: -0.1em;
}
```

## Replacing [Twemoji](https://github.com/twitter/twemoji)

Fluent Emoji offers a drop-in replacement for Twemoji. If you are currently using Twemoji, you can replace it with Fluent Emoji by simply replacing the Twemoji CDN URL with the Fluent Emoji CDN URL:

```html
<script src="https://emoji.fluent-cdn.com/latest/fluentemoji.min.js" crossorigin="anonymous"></script>
```

This works because Fluent Emoji ships with a Twemoji compatibility layer that allows it to be used as a drop-in replacement for Twemoji.

## Contact

Please feel free to [open a GitHub issue](https://github.com/AdvenaHQ/fluent-emoji/issues/new) with questions or requests.

## License

This project relies heavily on assets created and owned by Microsoft, and [Microsoft's Fluent Emoji project](https://github.com/microsoft/fluentui-emoji), which maintains it's own Code of Conduct and Licensing. Please refer to that repository for more information on the licensing of the emoji assets.

The code in this repository is licensed under the [MIT License](LICENSE).