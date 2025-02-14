# 北理良乡今天吃什么🍞

这是一个简单的网页应用程序，用于帮助你决定今天吃什么。专门为了北京理工大学良乡校区的选择困难症写的小页面。
链接如下：https://bit-eat-today.vercel.app/

## 文件结构🍭

- `index.html` - 主 HTML 文件
- `styles.css` - 样式文件
- `script.js` - 脚本文件

## 主要内容🧋

### HTML (`index.html`)

```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>今天吃什么</title>
    <link rel="stylesheet" href="./styles.css">
</head>

<body>
    <h1>今天吃什么？🌞</h1>
    <div class="container" id="container">
        <div class="loveheart">❤️</div>
        <p id="result">点击下方按钮开始</p>
        <button id="startbtn" onclick="pickFood()">让他帮我决定！</button>
    </div>

    <script src="./script.js"></script>
</body>

</html>
```

### CSS (`styles.css`)

```css
body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
    text-align: center;
    background-color: #f0f0f0;
}

h1 {
    margin-top: 20px;
    font-size: 2em;
}

.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    padding: 20px;
    box-sizing: border-box;
}

.loveheart {
    font-size: 3em;
    margin-bottom: 20px;
}

#result {
    font-size: 1.5em;
    margin-bottom: 20px;
}

button {
    padding: 10px 20px;
    font-size: 1em;
    cursor: pointer;
    border: none;
    border-radius: 5px;
    background-color: #007bff;
    color: white;
}

button:hover {
    background-color: #0056b3;
}

@media (max-width: 600px) {
    h1 {
        font-size: 1.5em;
    }

    .loveheart {
        font-size: 2em;
    }

    #result {
        font-size: 1.2em;
    }

    button {
        font-size: 0.9em;
        padding: 8px 16px;
    }
}
```

### JavaScript (`script.js`主要函数实现)

```javascript
function pickFood() {
    const foods = ["披萨", "汉堡", "寿司", "沙拉", "意大利面"];
    const randomIndex = Math.floor(Math.random() * foods.length);
    const resultElement = document.getElementById("result");
    resultElement.textContent = `今天吃 ${foods[randomIndex]} 吧！`;
}
```

## 说明🍬

- index.html 文件包含了网页的基本结构和内容。
- `styles.css` 文件定义了网页的样式，包括响应式设计，以确保在不同设备上显示良好。
- `script.js` 文件包含了 `pickFood` 函数，用于随机选择食物并显示在页面上。

通过以上文件，你可以创建一个简单的网页应用程序，帮助你决定今天吃什么。确保所有文件路径正确，并在浏览器中打开 index.html 文件以查看效果。
