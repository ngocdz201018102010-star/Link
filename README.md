# Link
Aim lock NEXTRON
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>FF Hack Menu - Demo</title>

<style>
body {
    margin: 0;
    background: #0a0a0a;
    font-family: -apple-system, BlinkMacSystemFont;
    color: white;
}

.menu {
    width: 92%;
    max-width: 360px;
    margin: 60px auto;
    background: #121212;
    border-radius: 18px;
    padding: 16px;
    box-shadow: 0 0 25px #ff000055;
}

.header {
    text-align: center;
    color: #ff3b3b;
    font-size: 22px;
    font-weight: bold;
}

.note {
    text-align: center;
    font-size: 12px;
    color: #aaa;
    margin-bottom: 15px;
}

.option {
    background: #1c1c1c;
    border-radius: 12px;
    padding: 12px;
    margin-bottom: 10px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.switch {
    width: 46px;
    height: 24px;
    background: #444;
    border-radius: 20px;
    position: relative;
}

.switch::after {
    content: "";
    width: 20px;
    height: 20px;
    background: white;
    border-radius: 50%;
    position: absolute;
    top: 2px;
    left: 2px;
    transition: 0.3s;
}

.switch.active {
    background: #ff3b3b;
}

.switch.active::after {
    left: 24px;
}

.footer {
    text-align: center;
    font-size: 11px;
    color: #666;
    margin-top: 10px;
}
</style>
</head>

<body>

<div class="menu">
    <div class="header">FREE FIRE MENU</div>
    <div class="note">HTML Demo • Education Only</div>

    <div class="option">
        Aim Assist (Demo)
        <div class="switch" onclick="toggle(this,'aim')"></div>
    </div>

    <div class="option">
        Fix Lag (Demo)
        <div class="switch" onclick="toggle(this,'lag')"></div>
    </div>

    <div class="option">
        Sensitivity Boost
        <div class="switch" onclick="toggle(this,'sens')"></div>
    </div>

    <div class="option">
        Headshot Mode
        <div class="switch" onclick="toggle(this,'head')"></div>
    </div>

    <div class="footer">
        Giả lập menu • Không hack thật
    </div>
</div>

<script>
function toggle(el,key){
    el.classList.toggle("active");
    localStorage.setItem(key, el.classList.contains("active"));
}

document.querySelectorAll(".switch").forEach(sw=>{
    let key = sw.getAttribute("onclick").split("'")[1];
    if(localStorage.getItem(key) === "true"){
        sw.classList.add("active");
    }
});
</script>

</body>
</html>