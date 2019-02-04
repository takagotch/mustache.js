### mustache.js
---
https://github.com/janl/mustache.js

```
npm install mustache --save
bower install --save mustache

npm install -g mustache
mustache dataView.json myTemplate.mustache > output.html

cat dataView.json | mustache - myTemplate.mustache > output.html

npm install mustache --save-dev

npm run build
mustache -p path/to/partial1.mustache -p path/to/partial2.mustache dataView.json myTemplate.mustache

rake jquery
rake mootools
rake dojo
rake yui3
rake qooxdoo

npm install
npm test

TEST=mytest npm run test-render
npm run test-browser-local
npm install -g npm
```

```
{
  "scripts": {
    "build": "mustache dataView.json myTemplate.mustache > public/output.html"
  }
}

{
  "name": "Tater",
  "bold": function(){
    return function(text, render){
      return "<b>" + render(text) + "</b>";
    }
  }
}

```

```js
var view = {
  title: "Joe",
  calc: function(){
    return 2 + 4;
  }
};
var output = Mustache.render("{{title}} spends {{calc}}", view);

Mustache.render(
  template : String,
  view : Object,
  partials> : Object,
  tags = ['{{', '}}'] : Tags,
) => String
Mustache.parse(
  template : String,
  tags = ['{{', '}}'] : Tags,
) => Token[]
interface Token [String, String, Number, Number, Token[]?, Number?]
interface Tags [String, String]

function loadUser(){
  var template = $('#template').html();
  Mustache.parse(template);
  var rendered = Mustache.render(template, {name: "Luke"});
  $('#target').html(rendered);
}

function loadUser(){
  $.get('template.mst', funciton(template){
    var rendered = Mustache.render(template, {name: "Luke"});
    $('#target').html(rendered);
  });
}

var customTags = [ '<%', '%>' ];
Mustache.render(template, view, {}, customTags)
Mustache.tags = customTags;
Mustache.parse(template);
Mustache.render(template, view);
```

