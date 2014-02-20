*This repository is a mirror of the [component](http://component.io) module [ecarter/css-emitter](http://github.com/ecarter/css-emitter). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/ecarter-css-emitter`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# css-emitter

  Bind functions to `transition` and `animation` events.

## Installation

    $ component install anthonyshort/css-emitter
  
or via npm for Browserify

    $ npm install css-emitter-component

## Example

    var css = require('css-emitter');
    var el = document.querySelector('#box');

    var animate = css(el);

    // Bind
    animate.bind(function(e){
      console.log('%s property changed on %s event', e.propertyName, e.type);
    });

    // Change height and width
    setTimeout(function(){
      el.className = 'in';
    }, 1000);

### Example CSS

    #box {
      width: 100px;
      height: 100px;
      transition: all 1s ease;
      -webkit-transition: all 1s ease;
      -moz-transition: all 1s ease;
      -o-transition: all 1s ease;
      background: black;
      display: block;
    }

    #box.in {
      width: 200px;
      height: 200px;
    }

## API

### CssEmitter(target:Element)

Initialize an `CssEmitter` with given `target` element.

### CssEmitter.bind(fn:Function)

Register bind function.

### CssEmitter.unbind([fn]:Function)

Unregister bind function.

### CssEmitter.once(fn:Function)

Register a function that will fire once then unbind automatically

## License

  MIT

