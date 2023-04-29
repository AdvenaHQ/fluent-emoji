<image src='art/images/banner.gif' alt='Microsoft Teams Animted emojis' />

# [Microsoft Teams](https://www.microsoft.com/en-us/microsoft-teams) Fluent Animated emojis

A simple library that provides standard Unicode emoji support across all platforms for Fluent Emoji. Fluent Emoji are a [collection of familiar, friendly, and modern emoji from Microsoft](https://github.com/microsoft/fluentui-emoji).

This library is also offered as a drop-in replacement for [twemoji](https://github.com/twitter/twemoji) which, due to recent changes at Twitter and the [deprecation of MaxCDN](https://github.com/twitter/twemoji#cdn-support), is no longer a viable option for many developers.

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
<script src="https://emoji.fluent-cdn.com/1.0.0/fluentemoji.min.js" crossorigin="anonymous"></script>
```

## Contact

Please feel free to [open a GitHub issue](https://github.com/AdvenaHQ/fluent-emoji/issues/new) with questions or requests.

## License

This project relies heavily on assets created and owned by Microsoft, and [Microsoft's Fluent Emoji project](https://github.com/microsoft/fluentui-emoji), which maintains it's own Code of Conduct and Licensing. Please refer to that repository for more information on the licensing of the emoji assets.

The code in this repository is licensed under the [MIT License](LICENSE).