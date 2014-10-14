AngularJS common library in your projects
=========================================

When you got more than one project you work on, then sharing code is what you want to do... don't repeat yours self principle.

```shell

piecArch@piecyk ~/projects/common-ui/src $ tree
.
├── app
│   ├── app-controller.js
│   ├── _app.js
│   ├── app.tpl.html
│   └── error-handler.example.tpl.html
├── directives
│   └── breadcrumbs
│      └── breadcrumbs-directive.js   
├── filters
│   └── unsafe-html
│       └── unsafe-html-filter.js
├── index.html
└── services
    ├── error-handler
    │   ├── error-handler-factory.js
    │   ├── _error-handler.js
    │   └── error-handler.tpl.html
    └── security-handler
        ├── secuirty-handler.spec.js
        └── secuirty-handler.js

```

```js
angular.module("common-ui", [
"common-ui.error-handler",
"common-ui.security-handler"
]);
```

