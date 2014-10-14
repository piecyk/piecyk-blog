AngularJS common library in your projects
=========================================

When you got more than one project you work on, then sharing code is what you want to do... don't repeat yourself principle.
The discussion is do we create separate projects for every component or we create one and build it in that why we can include
single dependency as it own... To achieve that we need to decide on some ground rules like convection how we create our "reusable"
parts of code.

```shell
piecArch@piecyk ~/projects/common-ui $ tree
.
├── bower_components
│   └── angular
├── bower.json
├── build.conf.js
├── dist
├── grunt
│   ├── bower.js
│   ├── clean.js
│   ├── compress.js
│   ├── jscs.js
│   ├── jshint.js
│   ├── karma.js
│   ├── customConcat.js
│   ├── customHtml2js.js
│   ├── customHtmlBuild.js
│   └── customUglify.js
├── Gruntfile.js
├── node_modules
├── package.json
├── README.md
├── src
│    ├── app
│    │   ├── app-controller.js
│    │   ├── _app.js
│    │   ├── app.tpl.html
│    │   └── error-handler.example.tpl.html
│    ├── directives
│    │   └── breadcrumbs
│    │      └── breadcrumbs-directive.js
│    ├── filters
│    │   └── unsafe-html
│    │       └── unsafe-html-filter.js
│    ├── index.html
│    └── services
│        ├── error-handler
│        │   ├── error-handler-factory.js
│        │   ├── _error-handler.js
│        │   └── error-handler.tpl.html
│        └── security-handler
│            ├── secuirty-handler.spec.js
│            └── secuirty-handler.js
└── test
    └── karma.conf.js

```

```js
angular.module("common-ui", [
"common-ui.error-handler",
"common-ui.security-handler"
]);
```
