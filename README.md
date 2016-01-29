dx-angularjs-modules
====================

Common utility modules used by most Angular applications but not provided by AngularJS, yet!

**How-to use this project with git subtree:**

1 - Create a git subtree into your project as follow:
```shell
git subtree add --prefix=src/main/webapp/js/modules/dx-angularjs-modules git@github.com:romajs/dx-angularjs-modules.git master --squash
```

2 - Any change from this project can be updated into your project:
```shell
git subtree pull --prefix=src/main/webapp/js/modules/dx-angularjs-modules git@github.com:romajs/dx-angularjs-modules.git master
```

3 - Also you can push any modification from your project inside the subtree:
```shell
git subtree push --prefix=src/main/webapp/js/modules/dx-angularjs-modules git@github.com:romajs/dx-angularjs-modules.git master
```
*PS: only if you have push permission, of course!*

## Ajax handler [dx.ajax.handler]

Http interceptor to handle ajax calls by the application, can be used to show and hide a loading modal for example.

### Dependencies

* ng

### Configuration

The following functions must be overwritten:

#### dxAjaxHandlerStart

Loaded when **any** ajax call has started.

##### Ex:

* TODO

#### dxAjaxHandlerStop

Loaded when **all** ajax call has been sttoped.

##### Ex:

* TODO

## Format [dx.format]

Allows any declared filter into the application modules to be used as formatter directive, all AngularJS built-in **ngModel** are supported as well **ngModel** module.

### Usage

* TODO

##### Ex:

* TODO

#### Injectable/controller

* TODO

#### Html

* TODO

##### Ex:

```html
<input type="text" dx-format="number:2" />
```

### Dependencies

* ng

### dxFormattersProvider

Allows application to create new formatters to be use together with the **dx-format** directive.

#### add

* TODO

##### Ex:

```js
dxFormattersProvider.add('foo', {
    format: function(value) {
        return value;
    },
    unformat: function(value) {
        return value;
    }
})
```

### Embedded filters

* percentage  

## Internationalization [dx.i18n]

Internatinalization easy as never.

### Dependencies

* ngLocale

### Recipes

#### Directive (A)

* TODO

##### Ex:

```html
<span>{{'app.greetings'|dxI18n}}</span>
```

#### Directive (E)

* TODO

##### Ex:

```html
<span dx-i18n="app.greetings"></span>
```

#### Filter

* TODO

##### Ex:

```html
<ul ng-repeat="item in items : dxI18n(item.type)">...</ul>
```

### Configuration

The resource bundle must be specified.

#### dxI18nProvider.setResourceBundle

Defines the current resource bundle for internatinalization

##### Ex:

```js
var messagesResourceBundle = {
	'app.title': 'Title',
	'app.greetings': 'Hello world'
};

dxI18nProvider.setResourceBundle(messagesResourceBundle);
```

## Growl Notifications [dx.growl.notifications]

* TODO

## Modal [dx.modal]

* TODO
