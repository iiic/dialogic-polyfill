# dialogic-polyfill
JS module polyfill for HTML dialog element.

Polyfill is in single javascript module file `dialogicPolyfill.mjs`. Include it into your site like this:

``` html
	<script type="module" src="/dialogicPolyfill.mjs" crossorigin="anonymous" integrity="sha256-dHKuaxOuwurk+H26C/fMr3WGod+O7AgrhBQ6b80qc/w="></script>
```

All other files like `example-usage.html` and `example.css` are there to help, but they are not needed for polyfill function.

About `dialog` element
---------------------

It's simple, status of dialog element is stored in `open` attribute, when this attribute is presented on element dialog is visually show. When not, dialog element is hidden. You can change status by native javascript functions `show()` and `close()` on `HTMLDialogElement`. Look into example file.

More detail info
---------------

This polyfill is in js module, and modules are in default `defer` (even if you didn't add attribute `defer`), it means loaded asynchronously and executed after the document has been parsed.

You can change this default behaviour by adding attribute `async`, but yout can't make it synchronous.

All browsers have `dialog` element styled, even if they didn't support function like `show()` and `close()`. (This is for example Firefox now).
