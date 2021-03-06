## Details

<span class="important-indicator"></span> This function modifies the calling collection instead of returning a new one.  Use of this function should be considered for performance in some cases, but otherwise should be avoided.  Consider using `eles.filter()` or `eles.remove()` instead.

<span class="important-indicator"></span> Use this function only on new collections that you create yourself, using `cy.collection()`.  This ensures that you do not unintentionally modify another collection.

## Examples

With a collection:

```js
var col = cy.collection(); // new, empty collection
var e = cy.$('#e');

col.merge( cy.nodes() );

col.unmerge( e );
```

With a selector:

```js
var col = cy.collection(); // new, empty collection

col.merge( cy.nodes() );

col.unmerge('#e');
```
