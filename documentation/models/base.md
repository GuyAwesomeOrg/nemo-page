# Base Model
This model serves as the root for all models, providing some of the basic functionality needed across the board.

`_model` - Abstract... cannot be instantiated from `_model`

## Methods

### getBase()
Gets the base element for the object. Will walk up its parent objects to find the closest one.

`@returns {Promise}` resolves to a WebElement of the appropriate base element to the object. If the object does not have a `_base` of its own, it walks up the parent objects until it finds one (or returns undefined).

### get()
alias to `getBase`. This function gets overridden by Element model.

`@returns {Promise}` resolves to a WebElement of the appropriate base element to the object. If the object does not have a `_base` of its own, it walks up the parent objects until it finds one (or returns undefined).


### isBasePresent()
Determines if the base is present or not. Will walk up its parent objects to find the closest one.

`@returns {Promise}` A promise that will resolve to true if the base is present and false otherwise. If the object does not have a `_base` of its own, it walks up the parent objects until it finds one. **NOTE** If nothing in the chain has a `_base`, this will throw an exception.
