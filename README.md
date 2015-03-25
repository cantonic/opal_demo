# README

All branches have an additional js file `app/assets/javascripts/other_asset.js` which is NOT required in `application.js`, but instead required separately in `app/views/layouts/application.html.erb`.

## branch: variant1
Application JS filename: `application.js`
method used for requiring javascript files: `//= require` (default)
Output from JavaScript console: 
```
other_asset.js?body=1:1 I am not required in application.js
runtime.js?body=1:1314 WARNING: LoadError: cannot load such file -- application
other_asset.js?body=1:1 I am not required in application.js
runtime.js?body=1:1314 WARNING: LoadError: cannot load such file -- other_asset
```
