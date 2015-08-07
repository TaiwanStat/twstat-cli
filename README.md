twstat cli tool
---

A cli tool for twstat development usage.

## Install 

```
sudo npm install -g twstat-cli
```

#### Build project

```
twstat chart-item.js
```

#### watch project

add watch option, will rebuild only the specific which is modifed.

```
twstat chart-item.js -w
```

#### Init your project

```
twstat init test
```

this command will extend a new object in `lists.json`

```js
  {
    "title": "test",
    "url": "test",
    "img": "images/test.png",
    "description": "Project description"
  },
```

and also create a new folder for your project, for this example it will create and new folder called `test` in root.

In side the folder there is a file called `index.hbs`

`index.hbs`:

```html
<!DOCTYPE html>
<head>
  {{> header}}
    <!-- my js & css -->
</head>
<body>
  {{> start}}
    <!-- my charts -->
  {{> end}}
    <!-- my js & css -->
  {{> footer}}
</body>
```
