# 4cut_coding

## 스파르타코딩클럽의 인생사진 쏙쏙 코딩네컷

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>coding_4cut</title>

    <link rel="stylesheet" href="./coding_4cut.css">
    <script type="text/javascript" src="coding_4cut.js"></script>
</head>

<body>
    <div class="container">
        <div class="photos">
            <div id="image1" class="photo-frame" onmouseover="showText(1)" onmouseout="hideText(1)"
                onclick="alertText(1)">
                <span id="desc1" class="photo-description">
                    첫 번째 이미지 설명
                </span>
            </div>
            <div id="image2" class="photo-frame" onmouseover="showText(2)" onmouseout="hideText(2)"
                onclick="alertText(2)">
                <span id="desc2" class="photo-description">
                    두 번째 이미지 설명
                </span>
            </div>
            <div id="image3" class="photo-frame" onmouseover="showText(3)" onmouseout="hideText(3)"
                onclick="alertText(3)">
                <span id="desc3" class="photo-description">
                    세 번째 이미지 설명
                </span>
            </div>
            <div id="vieo" class="photo-frame">
                <iframe src="https://www.youtube.com/embed/agYZbSt-3LY" frameborder="0" class="video"></iframe>
            </div>
        </div>

        <div class="footer">
            <p class="f-title">Happy Coding</p>
            <p class="f-date">2023.XX.XX</p>
        </div>
    </div>
</body>

</html>
```

```js
function showText(number) {
    if (number === 1) {
        document.querySelector("#desc1").classList.remove("hideText");
        document.querySelector("#desc1").classList.add("showText");
    } else if (number === 2) {
        document.querySelector("#desc2").classList.remove("hideText");
        document.querySelector("#desc2").classList.add("showText");
    } else {
        document.querySelector("#desc3").classList.remove("hideText");
        document.querySelector("#desc3").classList.add("showText");
    }
}

function hideText(number) {
    if (number === 1) {
        document.querySelector("#desc1").classList.remove("showText");
        document.querySelector("#desc1").classList.add("hideText");
    } else if (number === 2) {
        document.querySelector("#desc2").classList.remove("showText");
        document.querySelector("#desc2").classList.add("hideText");
    } else {
        document.querySelector("#desc3").classList.remove("showText");
        document.querySelector("#desc3").classList.add("hideText");
    }
}

function alertText(number) {
    alert(`${number}번째 추억이에요! 눌러주셔서 감사합니다 :)`);
}
```

```css
@font-face {
    font-family: "LeeSeoyun";
    src: url("https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_2202-2@1.0/LeeSeoyun.woff") format("woff");
    font-weight: normal;
    font-style: normal;
}

body {
    font-family: "LeeSeoyun";
    margin: 0;
    display: flex;
    justify-content: center;
    background-image: url("./img/background.png");
}

.container {
    width: 390px;
    background-color: #ff9d73;
    height: 100%;
}

.photos {
    margin-top: 30px;
}

.photo-frame {
    background-color: white;
    margin: 15px 20px;
    height: 200px;
    background-size: cover;
    position: relative;
    cursor: pointer;
}

.footer {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.f-title {
    font-size: 25px;
    font-weight: 900;
    color: white;
}

.f-date {
    font-size: 15px;
    font-weight: 500;
    color: white;
}

#image1 {
    background-image: url("./img/img1.png");
}

#image2 {
    background-image: url("./img/img2.png");
}

#image3 {
    background-image: url("./img/img3.png");
}

.photo-description {
    color: white;
    background-color: black;
    width: fit-content;
    padding: 0 20px;
    margin-bottom: 10px;
    border-radius: 10px;
    position: absolute;
    bottom: 0;
    transform: translate(-50%);
    left: 50%;
    opacity: 0;
}

.video {
    width: 100%;
    height: 100%;
}

.showText {
    opacity: 1;
    transition: opacity 0.5s linear;
}
```
