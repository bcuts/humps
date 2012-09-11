humps [![Build status](https://secure.travis-ci.org/domchristie/humps.png)](http://travis-ci.org/#!/domchristie/humps)
=====

Underscore-to-camelCase converter (and vice versa) for strings and object keys in JavaScript.

When converting object keys, it will walk the structure, converting any nested objects (or arrays of nested objects) along the way. Handy for converting JSON between JavaScript and Ruby/Rails APIs.

Takes inspiration from [Ember Data](https://github.com/emberjs/data) and copies some utility functions from [Underscore.js](http://underscorejs.org/).

Usage
-----

### Converting strings

    humps.camelize("hello_world"); // "helloWorld"
    humps.decamelize("fooBar"); // "foo_bar""

### Decamelizing strings with custom separator

    humps.decamelize("helloWorld", "-"); // "hello-world"

### Converting object keys
    
    var object = {
      attr_one: "foo",
      attr_two: "bar"
    };
    
    object = humps.camelizeKeys(object);
    
    object.attrOne === "foo"; // true
    object.attrTwo === "bar"; // true

Licence
-------
humps is copyright &copy; 2012 [Dom Christie](http://domchristie.co.uk) and released under the MIT license.