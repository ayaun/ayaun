<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>给你的一封告白信</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f0e5de;
            color: #333;
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        .message-box {
            padding: 40px;
            background-color: #fff;
            border-radius: 20px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            opacity: 0;
            transform: scale(0);
            transition: opacity 2s, transform 2s;
        }

        .message-box.active {
            opacity: 1;
            transform: scale(1);
        }

        h1 {
            font-size: 36px;
            color: #ff6f61;
            margin-bottom: 20px;
            font-family: 'Georgia', serif;
        }

        p {
            font-size: 20px;
            color: #555;
            line-height: 1.6;
        }

        .heart {
            font-size: 60px;
            color: red;
            margin: 20px 0;
        }

        .button {
            background-color: #ff6f61;
            color: white;
            padding: 12px 25px;
            font-size: 18px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .button:hover {
            background-color: #ff4b3a;
        }
    </style>
</head>
<body>

    <div class="message-box" id="messageBox">
        <h1>亲爱的 [小赵]</h1>
        <p>每次想到你，我的心就会加速跳动。<br>
        我想对你说——</p>
        <div class="heart">❤️</div>
        <p><strong>我喜欢你</strong><br>从第一次见面到现在，我发现自己越来越离不开你。</p>
        <button class="button" id="showButton">点击接受我的告白！</button>
    </div>

    <script>
        // 等待页面加载完成后，显示告白内容
        window.onload = function() {
            setTimeout(function() {
                document.getElementById('messageBox').classList.add('active');
            }, 500);
        }

        // 点击按钮后显示告白的最终确认
        document.getElementById('showButton').addEventListener('click', function() {
            alert("你答应了我吗？😊");
            document.getElementById('showButton').innerText = "我知道你会答应的！";
            document.getElementById('showButton').style.backgroundColor = "#ff4b3a";
        });
    </script>
    
</body>
</html>
