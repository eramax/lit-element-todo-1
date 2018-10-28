# LitElement TodoMVC Example

Implements all features of [TodoMVC](http://todomvc.com/) using [@polymer/lit-element](https://www.npmjs.com/package/@polymer/lit-element) (0.6.2).

## Learnings

* Mimic built-in html elements
  * Attrs/props in, events out
  * Naming too e.g. todo-list, todo-item, todo-form
* Shorthand type no longer supported for declared props e.g. _todos: Array
* Must call super first in a constructor
* this._abc is "protected"
* Make computed props getters or just compute in render()
* Use <slot> effectively
* Consider reflect:true to keep attrs updated
* Use object spread to keep render templates concise
* Auto update mechanism expects immutable props
* Default type for declared properties is String
* Double quotes in template attrs are only needed when value has spaces
* Events dispatched don't bubble by default
* To know when slot elements change use slotchange event
* Most element templates should style :host {display: block;}
  * When doing so be sure to set :host([hidden]) {display: none;}
* Reusable elements should "work" on their own without centralized state mgmt
* Don't use superflous elements in templates
* Allow styling of shadow dom elements with css variables
* Dispatch events after updating the state of an element
* Prefer all lower-case for custom event names
* Be careful not to override user settings when setting props and attrs on the root
* For checkboxes prefer the property .checked over attr ?checked
* [More...](https://developers.google.com/web/fundamentals/web-components/best-practices)