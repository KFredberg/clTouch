[![Climber - clTouch](https://github.com/kfredberg/clTouch/blob/master/cl-touch_large.png)](https://www.climber.eu)

Climber Touch Directives

A qvangular module to add directives for Qlik Sense input events. Useful when using ng-repeat.

![clTouch 1.0](https://img.shields.io/badge/clTouch-1.0-green.svg?style=flat)
[![Github All Releases](https://img.shields.io/github/downloads/KFredberg/clTouch/total.svg?maxAge=2592000)](https://github.com/KFredberg/clTouch/downloads)
[![GitHub stars](https://img.shields.io/github/stars/KFredberg/clTouch.svg)](https://github.com/KFredberg/clTouch/stargazers)
[![Issues](https://img.shields.io/github/issues/KFredberg/clTouch.svg)](https://github.com/KFredberg/clTouch/issues)
[![Forks](https://img.shields.io/github/forks/KFredberg/clTouch.svg)](https://github.com/KFredberg/clTouch/network)


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

Add the file in the define function in your extensions main js file. Example below clTouch.js is in a subfolder of the extension folder /lib/js/.

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

````
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

[![Climber - clTouch](https://github.com/kfredberg/clTouch/blob/master/climber-logo_small.png)](https://www.climber.eu)
