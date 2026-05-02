<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <!-- 关键：适配移动端，禁止放大缩小，让页面按设备宽度正常显示 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>三代嫂嫂来了</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "Microsoft Yahei", sans-serif;
        }

        /* 初始页面样式 - 整体缩小适配 */
        .page1 {
            width: 100vw;
            height: 100vh;
            background-color: #f8e6eb;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            position: relative;
        }

        /* 装饰元素缩小 */
        .flower {
            position: absolute;
            top: 30%;
            right: 15%;
            width: 40px;
            height: 40px;
            background: url('data:image/svg+xml;utf8,<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><path fill="%23ffb6c1" d="M50 5c-5 15-20 25-35 25 10 10 15 25 15 40 15-5 30-5 45 0 0-15 5-30 15-40-15 0-30-10-35-25z"/><circle fill="%23ffd700" cx="50" cy="50" r="10"/></svg>') no-repeat center center;
            background-size: contain;
        }
        .heart {
            position: absolute;
            bottom: 30%;
            left: 15%;
            width: 35px;
            height: 35px;
            background: url('data:image/svg+xml;utf8,<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><path fill="%23ff69b4" d="M50 85c-10-8-30-20-30-40 0-15 12-25 30-15 18-10 30 0 30 15 0 20-20 32-30 40z"/></svg>') no-repeat center center;
            background-size: contain;
        }

        /* 主标题缩小 */
        .main-title {
            font-size: 3rem;
            color: #b83259;
            font-weight: bold;
            margin-bottom: 15px;
        }

        /* 副标题缩小 */
        .sub-title {
            font-size: 1.1rem;
            color: #b83259;
            margin-bottom: 50px;
        }

        /* 按钮缩小 */
        .enter-btn {
            padding: 15px 60px;
            font-size: 1.5rem;
            color: white;
            background-color: #e07a9c;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }
        .enter-btn:hover {
            background-color: #d06085;
            transform: translateY(-2px);
        }

        /* 第二页样式 - 整体缩小适配 */
        .page2 {
            width: 100vw;
            height: 100vh;
            background-color: #ffffd1;
            display: none;
            align-items: center;
            justify-content: center;
            position: relative;
        }
        .chevron-left {
            position: absolute;
            top: 10%;
            left: 10%;
            width: 60px;
            height: 45px;
            background: url('data:image/svg+xml;utf8,<svg viewBox="0 0 100 60" xmlns="http://www.w3.org/2000/svg"><path fill="%23fce38a" d="M10 0h30v20H20v20h20v20H10zM60 0h30v20H70v20h20v20H60z"/></svg>') no-repeat center center;
            background-size: contain;
        }
        .rect {
            position: absolute;
            bottom: 10%;
            right: 10%;
            width: 45px;
            height: 8px;
            background-color: #fce38a;
        }
        .chevron-right {
            position: absolute;
            top: 10%;
            right: 10%;
            width: 60px;
            height: 45px;
            background: url('data:image/svg+xml;utf8,<svg viewBox="0 0 100 60" xmlns="http://www.w3.org/2000/svg"><path fill="%23fce38a" d="M10 0h30v20H20v20h20v20H10zM60 0h30v20H70v20h20v20H60z"/></svg>') no-repeat center center;
            background-size: contain;
            transform: scaleX(-1);
        }
        .text {
            font-size: 3.5rem;
            color: #333333;
            font-weight: bold;
        }

        /* 适配手机端的额外调整 */
        @media (max-width: 600px) {
            .main-title {
                font-size: 2.2rem;
            }
            .sub-title {
                font-size: 0.95rem;
            }
            .enter-btn {
                padding: 12px 50px;
                font-size: 1.3rem;
            }
            .text {
                font-size: 2.8rem;
            }
        }
    </style>
</head>
<body>
    <!-- 第一页：进入界面 -->
    <div class="page1" id="page1">
        <div class="flower"></div>
        <div class="heart"></div>
        <div class="main-title">三代嫂嫂来了</div>
        <div class="sub-title">TF三代 · 地下恋模拟器</div>
        <button class="enter-btn" onclick="goToPage2()">点击进入</button>
    </div>

    <!-- 第二页：整蛊界面 -->
    <div class="page2" id="page2">
        <div class="chevron-left"></div>
        <div class="chevron-right"></div>
        <div class="rect"></div>
        <div class="text">你被我骗了</div>
    </div>

    <script>
        function goToPage2() {
            document.getElementById('page1').style.display = 'none';
            document.getElementById('page2').style.display = 'flex';
        }
    </script>
</body>
</html>
