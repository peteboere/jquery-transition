
CSS transitions plugin for jQuery
=====

* Provides CSS transitions with an API similar to `jQuery.animate`
* Falls back to `jQuery.animate` for browsers that don't support CSS transitions
* Vendor prefixes not required


API
==================

    .transition( properties [, duration] [, easing] [, complete] )

* **properties**
	A map of CSS properties that the animation will move toward.
* **duration**
	A string or number determining how long the animation will run.
* **easing** 
	A string or object* indicating which easing function to use for the transition.  
	Different easing value can be specified for CSS transition and the fallback `jQuery.animate`  
	e.g. `{ transition: 'cubic-bezier(0,0,0.58,1)', animate: 'swing' }`
* **complete**
	A function to call once the animation is complete.


Example
==================

    $( 'div' ).transition({ 
    	'margin-top': 100,
    	'width': 300,
    	'transform': 'rotate(360deg)'
    }, 'slow', 'ease-in-out', function () {
    	console.log( 'Complete!' );
    });


Caveats
==================
Due to the nature of CSS transitions, it is not possible to recreate all the features of regular jQuery animation.
( See http://ejohn.org/blog/css-animations-and-javascript/ )

Relative property values (e.g.'+=100') are not supported when using jQuery version < 1.6