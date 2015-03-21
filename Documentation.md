

# Documentation #

## Function.prototype.bind ##
https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function/bind

## JavaScript 1.6 arrays ##
JavaScript version 1.6 specifies seven new methods for Array instances. These are implemented in oz.js, so you can use them even in pre-1.6 browsers (IE, Opera, Safari). For function reference, see http://www.webreference.com/programming/javascript/ncz/column4/index.html.

## Styles ##
  * **OZ.Style.get**(node, property) - retrieve current CSS property of a given node
  * **OZ.Style.set**(node, style) - set multiple CSS properties at once, including simple floating and opacity

## DOM helpers ##
  * **OZ.DOM.elm**(name, options) - create new DOM element and set many properties (styles and attributes)
  * **OZ.DOM.text**(string) - create new text node and set its contents
  * **OZ.DOM.clear**(node) - remove all children from a given node
  * **OZ.DOM.pos**(node) - return position (2 item array) of node relative to viewport
  * **OZ.DOM.scroll**() - return amount (2 item array) of horizontal and vertical scrolling
  * **OZ.DOM.win**() - return dimensions (2 item array) of document window
  * **OZ.DOM.hasClass**(node, className) - check whether given node has certain CSS class
  * **OZ.DOM.addClass**(node, className) - add a CSS class to DOM node
  * **OZ.DOM.removeClass**(node, className) - remove a CSS class from DOM node
  * **OZ.DOM.append**(arr1, arr2, ...) - append many DOM nodes with a single call

## Event management ##
  * **OZ.Event.add**(node || object, name, callback) - add event handler to DOM node or JS class, custom event names are supported. Multiple event names can be specified, space-separated. Callback always in context of attached DOM element.
  * **OZ.Event.remove**(event) - remove previously added event
  * **OZ.Event.target**(event) - get target element
  * **OZ.Event.prevent**(event) - prevent browser's default behavior
  * **OZ.Event.stop**(event) - stop event bubbling

## Classes ##
  * **OZ.Class**() - create base class
  * **OZ.Class().implement**(otherClass) - inherit prototype methods and properties from parent class
  * **OZ.Class().extend**(otherClass) - inherit prototype methods and properties from parent class; `child instanceof parent`
  * **OZ.Class().prototype.dispatch**(name, data) - dispatch custom event
  * **OZ.Class().prototype.bind**(method) - bind method to instance scope

## XML HTTP Request ##
  * **OZ.Request**(url, callback, options) - perform an asynchronous HTTP request

## Miscellaneous ##
  * **OZ.$**(id) - convert id to node
  * **OZ.opera** - is browser Opera?
  * **OZ.ie** - is browser Internet Explorer?
  * **OZ.gecko** - is browser Gecko-based?
  * **OZ.webkit** - is browser WebKit-based?
  * **OZ.khtml** - is browser KHTML-based?