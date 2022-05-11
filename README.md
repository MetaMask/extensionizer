# Extensionizer [DEPRECATED]

## Deprecation notice

This package has been deprecated in favor of [`webextension-polyfill`](https://github.com/mozilla/webextension-polyfill). We will not be maintaining this package anymore. Please consider migrating to `webextension-polyfill`.

## A module for writing cross-browser extensions

Most browsers (other than Safari) have implemented the [WebExtensions](https://developer.mozilla.org/en-US/Add-ons/WebExtensions) API for writing browser extensions.

Unfortunately, they've often hidden that common API under a variety of differently named global objects.

When you import `extensionizer`, it grabs those `WebExtension` APIs from wherever they're hiding, and hangs them all on a singleton object that it returns to you.

Just use `extensionizer` instead of the browser specific extension prefixing.

## Sample Usage

First install with `yarn install extensionizer`.

```javascript
const extension = require('extensionizer')

// Ever notice you can't use normal hyperlinks in an extension?
// Now it's easy:
extension.tabs.create({url: 'mailto:help@metamask.io?subject=Feedback'})

const manifest = extension.runtime.getManifest()
```

For the full list of supported methods, refer to the [MDN API documentation](https://developer.mozilla.org/en-US/Add-ons/WebExtensions/API).

## Running Tests

Run `yarn test` after running `yarn`.
