
#Backback

Backpack is a boilerplate project for personal Backbone.js projects which includes some common items I use in my setup. It is based on a fork of [jbasdf](https://github.com/jbasdf/requirejs-backbone-example)'s Backbone.js template.

###Included in the backpack are:

* Backbone.js (AMD patched)
* Underscore.js (AMD patched)
* jQuery.js
* Require.js (latest)
* i18n.js plugin for RequireJS
* text plugin for RequireJS
* jQuery Cookies plugin 
* Almond
* r.js with instructions to build the project
* Jasmine for BDD testing


##Summary

The build process will run the application through r.js, replacing require.js with almond.js in production. Information about how the project is built can be found in the app.build.js file in ```public\js```. 

##Building

If you have node installed, the project can be built by running:

```node public/js/app.build.js```

If you would prefer a rake task that completes this task, try:

```rake build```

##Using the project

The backpack comes with a Sinatra application for serving up assets. You'll need both [ruby](http://www.ruby-lang.org/en/downloads/) and bundler installed in order to run this. To get bundler, simply run:

```gem install bundler```
 
Follow the instructions at the ruby link above to download and install that dependency. The project can then be run using:

```ruby app.rb```

This will give you the ability to access three URLs:

http://localhost:4567  
http://localhost:4567/dev
http://localhost:4567/jquery (how require.js will prefer the jQuery version loaded in the page to the one stated in the project)

##Patched AMD Backbone and Underscore builds

Backpack already contains patched AMD-compatible versions of Backbone.js and Underscore.js but if wish to grab the latest patched versions of these libraries they can be accessed from:

* https://github.com/amdjs/underscore
* https://github.com/amdjs/backbone


