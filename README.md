# dialogic-polyfill

> **⚠️ DEPRECATED:** This project is deprecated and no longer maintained, please don't use it in new projects.
>
> A possible successor is **[Dialogic](https://github.com/iiic/Dialogic)** – popups built on the native `<dialog>` element with the same API as the browser's `Notification()`. It isn't a polyfill and has a different API, so it's not a drop-in replacement.
>
> The `dialog` element itself is natively supported by all modern browsers today, so you most likely don't need any polyfill for it.

JS module polyfill for HTML dialog element. Simple, easy to use, **No dependencies**, just vanilla js.

Polyfill is in single javascript module file `dialogicPolyfill.mjs`. Include it into your site like this:

``` html
	<script type="module" src="/dialogicPolyfill.mjs" crossorigin="anonymous" integrity="sha256-PQWC6KjeQE1GHATV6Tj7tz4ccuHICdpyVLvzOn1UZpU="></script>
```

That's it! Now you can use dialog element like you know from specification [MDN: The Dialog element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dialog) and it will work even in browsers that doesn't have full support for dialog yet.

All other files like `example-usage.html` and `example.css` are there to help, but they are not needed for polyfill function.

About `dialog` element
---------------------

It's simple, status of dialog element is stored in `open` attribute, when this attribute is presented on element dialog is visually show. When not, dialog element is hidden. You can change status by native javascript functions `show()` and `close()` on `HTMLDialogElement`. Look into example file.

More detail info
---------------

This polyfill is in js module, and modules are in default `defer` (even if you didn't add attribute `defer`), it means loaded asynchronously and executed after the document has been parsed.

You can change this default behaviour by adding attribute `async`, but yout can't make it synchronous.

All browsers have `dialog` element styled, even if they didn't support function like `show()` and `close()`. (This is for example Firefox now).

Services
--------

Unpkg: https://unpkg.com/dialogic-polyfill

NPM: https://www.npmjs.com/package/dialogic-polyfill


# Licence

**CC BY-SA 4.0**

This work is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by-sa/4.0/ or send a letter to Creative Commons, PO Box 1866, Mountain View, CA 94042, USA.

-------

more info at https://iiic.dev/dialogic-polyfill
