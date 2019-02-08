### hogan.js
---
https://github.com/twitter/hogan.js

```js
var data = {
  screenName: "dhg",
};
var template = Hogan.compile("Follow @{{screenName}}.");
var output = template.render(data);

console.log(output);


var text = "{{^check}}{{#i18n}}No{{/i18n}}{{/check}}";
text += "{{#check}}{{#i18n}}Yes{{/i18n}}{{/check}}";
var tree = Hogan.parse(Hogan.scan(text));
console.log(tree[0].tag + " " + tree[0].name);
console.log(tree[1].nodes[0].nodes[0]);

var text = "my <%example%> template."
Hogan.compile(text, {delimiters: '<% %>'});

var text = "{{_foo}}example{{/foo}} template."
Hogan.compile(text, { sectionTags: [{o: '_foo', c: 'foo'}]]);
```

```
npm install hogan.js

component install twitter/hogan.js

node test/spec.js
```

```
```

