* `@State` 
	- used for propreties like Strings, integers, and Booleans
	- only for use in a single view, generally should be marked private
	- if used with an object, a view update will only be triggered when the reference changes (ie the variable now holds a new object)

* `@ObservedObject` 
	- complex propreties, like custom types (also allows for sharing data across multiple views)
	- used with reference types
* `@Binding` 
	-  “A binding connects a property to a source of truth stored elsewhere, instead of storing data directly.”
	- a `value` is owned by another object (`@State` -> `@Binding`)
	- if used with an object, a view update will only be triggered when the reference changes (ie the variable now holds a new object)
	
$variableName 
	- a two way relationship, the view `$variableName` is passed to can modify it and the view that owns `$variableName` will update
