# nhim-secret
Secret IC3 project
<!DOCTYPE html>
<html>
<head>
  <title>Bí mật 😏</title>
  <style>
    body {
      background: black;
      color: lime;
      text-align: center;
      font-family: Arial;
      margin-top: 100px;
    }
    input, button {
      padding: 10px;
      font-size: 16px;
      margin: 5px;
    }
    #rickroll {
      display: none;
    }
  </style>
</head>
<body>

<h2>🔐 Nhập mật khẩu</h2>

<input type="password" id="pass1">
<button onclick="check1()">Mở khóa</button>

<div id="hint1"></div>

<div id="rickroll">
  <h2>😆 Xin lỗi nha!</h2>

  <img src="https://media.giphy.com/media/Vuw9m5wXviFIQ/giphy.gif" width="300">

  <p>🔐 Nhập mật khẩu tiếp:</p>
  <input type="password" id="pass2">
  <button onclick="check2()">Tiếp tục</button>

  <div id="hint2"></div>
  <div id="final"></div>
</div>

<script>
function check1() {
  var p = document.getElementById("pass1").value;

  if (p === "27032015") {
    document.body.innerHTML = document.getElementById("rickroll").outerHTML;
    document.body.style.background = "black";
    document.body.style.color = "lime";
  } else {
    document.getElementById("hint1").innerHTML =
      "❌ Sai rồi! Gợi ý: mật khẩu là sinh nhật của người đang ngồi trước màn hình 😆";
  }
}

function check2() {
  var p2 = document.getElementById("pass2").value;

  if (p2 === "20032014") {
    document.getElementById("hint2").innerHTML = "⏳ Đang kiểm tra...";

    setTimeout(function() {
      document.getElementById("final").innerHTML =
        "🎉 Chúc mừng, bạn là người độc quyền giải ra những mật khẩu tuyệt vời nhất!";
    }, 2000);

  } else {
    document.getElementById("hint2").innerHTML =
      "❌ Sai rồi! Gợi ý: ngày sinh của người làm trang web 😏";
  }
}
</script>

</body>
</html>
