# css画loading

### 效果预览 - 01
![](images/loading.gif)

### 源代码 - 01
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>css loading</title>

    <style>
      .ma-mskLoading {
        width: 100%;
        height: 100vh;
        background: #ffffff;
        display: flex;
        align-items: center;
        justify-content: center;
        box-sizing: border-box;
      }

      .ma-line-scale > div {
        /* background-color: #c1c1c1; */
        background-color: #607d8b;
        width: 4px;
        height: 35px;
        border-radius: 2px;
        margin: 2px;
        -webkit-animation-fill-mode: both;
        animation-fill-mode: both;
        display: inline-block;
      }

      .ma-line-scale > div:first-child {
        -webkit-animation: line-scale-data 1s cubic-bezier(0.2, 0.68, 0.18, 1.08) -0.4s infinite;
        animation: line-scale-data 1s cubic-bezier(0.2, 0.68, 0.18, 1.08) -0.4s infinite;
      }

      .ma-line-scale > div:nth-child(2) {
        /* -webkit-animation:line-scale-data 1s cubic-bezier(.2,.68,.18,1.08) -.3s infinite; */
        animation: line-scale-data 1s cubic-bezier(0.2, 0.68, 0.18, 1.08) -0.3s infinite;
      }

      .ma-line-scale > div:nth-child(3) {
        -webkit-animation: line-scale-data 1s cubic-bezier(0.2, 0.68, 0.18, 1.08) -0.2s infinite;
        animation: line-scale-data 1s cubic-bezier(0.2, 0.68, 0.18, 1.08) -0.2s infinite;
      }

      .ma-line-scale > div:nth-child(4) {
        -webkit-animation: line-scale-data 1s cubic-bezier(0.2, 0.68, 0.18, 1.08) -0.1s infinite;
        animation: line-scale-data 1s cubic-bezier(0.2, 0.68, 0.18, 1.08) -0.1s infinite;
      }

      .ma-line-scale > div:nth-child(5) {
        -webkit-animation: line-scale-data 1s cubic-bezier(0.2, 0.68, 0.18, 1.08) 0s infinite;
        animation: line-scale-data 1s cubic-bezier(0.2, 0.68, 0.18, 1.08) 0s infinite;
      }

      @-webkit-keyframes line-scale-data {
        0% {
          -webkit-transform: scaley(1);
          transform: scaley(1);
        }

        50% {
          -webkit-transform: scaley(0.4);
          transform: scaley(0.4);
        }

        to {
          -webkit-transform: scaley(1);
          transform: scaley(1);
        }
      }

      @keyframes line-scale-data {
        0% {
          -webkit-transform: scaley(1);
          transform: scaley(1);
        }

        50% {
          -webkit-transform: scaley(0.4);
          transform: scaley(0.4);
        }

        to {
          -webkit-transform: scaley(1);
          transform: scaley(1);
        }
      }
    </style>
  </head>
  <body>
    <div id="app">
      <div class="ma-mskLoading">
        <div class="ma-line-scale">
          <div></div>
          <div></div>
          <div></div>
          <div></div>
          <div></div>
        </div>
      </div>
    </div>
  </body>
</html>

```

---

### 效果预览 - 02
![](images/loading2.gif)

### 源代码 - 02
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>css loading2</title>
    <style>
        .wrapper {
            width: 600px;
            height: 400px;
            margin: 30px auto;
            background: #f7f7f7;
            box-shadow: 1px 2px 5px #ccc;
            position: relative;
        }
        .wrapper::after {
            content: '';
            position: absolute;
            left: 50%;
            top: 50%;
            margin-top: -20px;
            margin-left: -20px;
            border-top: 2px solid #8FBC8F;
            border-right: 2px solid transparent;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            animation: loading .9s cubic-bezier(.33,.55,.97,.98) infinite ;
        }

        @keyframes loading{
            from {
                transform: rotate(0); 
            }
            to {
                transform: rotate(360deg);
            }
        }
    </style>
</head>
<body>
    <div class="wrapper"></div>
</body>
</html>

```
