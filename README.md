# README

All branches have an additional js file `app/assets/javascripts/other_asset.js` which is NOT required in `application.js`, but instead required separately in `app/views/layouts/application.html.erb`.

## branch: variant1
Application JS filename: `application.js`

method used for requiring javascript files: `//= require` (default)

Output from JavaScript console: 
```
included_asset.js?body=1:1 I am required in application.js
runtime.js?body=1:1314 WARNING: LoadError: cannot load such file -- application
separate_asset.js?body=1:1 I am NOT required in application.js
runtime.js?body=1:1314 WARNING: LoadError: cannot load such file -- separate_asset
```

## branch: variant2
Application JS filename: `application.js.rb`

method used for requiring javascript files: `//= require` (default)

Output from JavaScript console: 
```
included_asset.js?body=1:1 I am required in application.js
separate_asset.js?body=1:1 I am NOT required in application.js
```

## branch: variant3
Application JS filename: `application.js.rb`

method used for requiring javascript files: `require` (Ruby's require method)

Output from JavaScript console: 
```
included_asset.js?body=1:1 I am required in application.js
separate_asset.js?body=1:1 I am NOT required in application.js
```
