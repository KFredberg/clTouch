Climber Touch Directives

A qvangular module to add directives for Qlik Sense input events.


* [Info](#info)
* [Installing](#installingloading)
* [Usage](#usage)
* [License](#license)

## Info

Version: 1.0.0    
Author: Karl Fredberg [[Github](https://github.com/kfredberg)] [[Twitter](https://twitter.com/Controllanten)]  

cl-activate
cl-swipestart
cl-swipeupdate
cl-swipecancel
cl-swipe  

## Installing

Copy clTouch.js into your extension directory.

Add the file in the define function in your extensions main js file. Example below clTouch.js is in a subfolder of the extension /lib/js/.

```
define([
        'jquery',
        './properties',
        './initialproperties',
        'text!./lib/css/style.css',
        'text!./lib/partials/template.html',
        './lib/js/clTouch'
    ],
```

## Usage

Add the attributes to the elements in your template:
````
<div ng-repeat="item in items" 
	 cl-swipestart="onSwipestart($event)" 
	 cl-swipeupdate="onSwipeupdate($event)" 
	 cl-swipe="onSwipe($event)">{{item.title}}</div>
````
In your controller in your mainExtensionFile.js add the functions you refered to in the template

$scope.onSwipestart = function($event) {
   console.log('touchstart event called');
}
$scope.onSwipeupdate = function($event) {
   console.log('touchstart event called');
}
$scope.onSwipe = function($event) {
   console.log('touchstart event called');
}
```

## License

Released under the MIT License - see [`license.txt`](https://github.com/kfredberg/clTouch/blob/master/license) for details.
