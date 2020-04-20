# jQuery Event Basics
jQuery offers convenience methods for most native browser events. 
These methods - including 
* ```click() ```
* ```focus() ```
* ```blur() ```
* ```change() ```
* ```etc.``` 		

 are shorthand for jQuery's  ``` .on()``` method. 

It is important to note that .on() can only create event listeners on 
elements that exist <b color=red>at the time you set up the listeners.

Every event handling function receives an event object, which contains many properties and methods.
<p>Event object contains a number of other useful properties and methods, including:

* <b>pageX, pageY</b> - The mouse position at the time the event occurred, relative to the top left corner of the page display area (not the entire browser window).
* <b>type</b> - The type of the event (e.g., "click").
* <b>which</b> - The button or key that was pressed.
* <b>data</b> - Any data that was passed in when the event was bound
* <b>target</b> - The DOM element that initiated the event.
* <b>namespace</b> - The namespace specified when the event was triggered.
* <b>timestamp</b> - The difference in milliseconds between the time the event occurred in the browser and January 1, 1970.
* <b>preventDefault()</b>  - Prevent the default action of the event (e.g. following a link).
* <b>etc.</b> 

To turn the DOM element into a jQuery object that we can use jQuery methods on, we simply do $( this ), often following this idiom:

```javascript
var element = $( this );
```

## Multiple events, same handler
``` 
$( "input" ).on(
    "click change", // Bind handlers for multiple events
    function() {
        console.log( "An input was clicked or changed!" );
    }
);
```
## Binding multiple events with different handlers
```
$( "p" ).on({
    "click": function() { console.log( "clicked!" ); },
    "mouseover": function() { console.log( "hovered!" ); }
});
```