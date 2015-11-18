twstat cli tool
---

A cli tool for twstat development usage.

## Install 

```
sudo npm install -g twstat-cli
```

#### Build project

```
twstat chart_item.js
```

#### watch project

add watch option, will rebuild only the specific which is modifed.

```
twstat chart-item.js -w
```

### minify project

```
twstat chart-item.js -m
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
<html xmlns="http://www.w3.org/1999/xhtml" lang='zh-TW'>
  <head>
    {{> head}}
    <!-- my js & css -->
    <link rel="stylesheet" type="text/css" href="./css/style.css">
  </head>
  <body>
    {{> header}}
    {{> start}}
    <!-- my charts -->
    <div class="chart">

    </div>
    {{> end}}
    <!-- my js & css -->
    {{> footer}}
    <script type="text/javascript" src="./js/index.js"></script>
  </body>
</html>
```

and also have empty css and js file in the folder.
