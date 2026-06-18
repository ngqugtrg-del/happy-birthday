# happy-birthday<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🎂 Chúc Mừng Sinh Nhật 🎂</title>

    <style>
        *{
            margin:0;
            padding:0;
            box-sizing:border-box;
        }

        body{
            background:linear-gradient(135deg,#ff9ec4,#ffd6e7);
            overflow:hidden;
            font-family:Arial,sans-serif;
            display:flex;
            justify-content:center;
            align-items:center;
            height:100vh;
        }

        .card{
            text-align:center;
            background:white;
            padding:40px;
            border-radius:20px;
            box-shadow:0 10px 30px rgba(0,0,0,.2);
            z-index:10;
        }

        h1{
            color:#ff4081;
            margin-bottom:20px;
        }

        p{
            font-size:20px;
            color:#444;
            margin-top:10px;
        }

        .heart{
            position:absolute;
            color:red;
            animation:float 8s linear infinite;
            font-size:20px;
        }

        @keyframes float{
            from{
                transform:translateY(100vh);
                opacity:1;
            }

            to{
                transform:translateY(-100px);
                opacity:0;
            }
        }

        button{
            margin-top:25px;
            padding:12px 25px;
            border:none;
            border-radius:50px;
            background:#ff4081;
            color:white;
            font-size:18px;
            cursor:pointer;
        }

        button:hover{
            background:#ff1f6b;
        }
    </style>
</head>

<body>

<div class="card">
    <h1>🎉 Happy Birthday 🎉</h1>

    <h2>Chúc mừng sinh nhật ❤️</h2>

    <p>
        Chúc bạn luôn vui vẻ,<br>
        hạnh phúc,<br>
        luôn mỉm cười mỗi ngày. 💕
    </p>

    <button onclick="alert('🎂 Chúc bạn sinh nhật thật nhiều niềm vui ❤️')">
        Nhấn vào đây 🎁
    </button>

</div>

<script>

function createHeart(){

    let heart=document.createElement("div");

    heart.className="heart";

    heart.innerHTML="❤";

    heart.style.left=Math.random()*100+"vw";

    heart.style.fontSize=(20+Math.random()*30)+"px";

    heart.style.animationDuration=(5+Math.random()*5)+"s";

    document.body.appendChild(heart);

    setTimeout(()=>{
        heart.remove();
    },9000);

}

setInterval(createHeart,250);

</script>

</body>
</html>
