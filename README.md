amd-parse
=========

AMD-enabled version of Parse.com official JavaScript library (v. 1.2.8) https://www.parse.com/downloads/javascript/parse/latest/js

Example usage with require.js
=============================

// main.js

require.config({
    paths: {
        jquery: 'libs/jquery',
        underscore: 'libs/underscore',
        parse: 'libs/parse'
    }
});
require([
      'app'
    ], function(App){
      // The "app" dependency is passed in as "App"
      App.initialize();
    }
);

// app.js

define([
    'jquery',
    'underscore',
    'parse',
    'router'
    ], 
    function($, _, Parse, Router){
        var initialize = function(){
            Parse.initialize("application-id", "your-key");
        }
        return {
            initialize: initialize
        }; 
    }
);


