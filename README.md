<!--# hello-world-->
<!--my frist github -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>hello world</title>
</head>
<body>
<input type="button" id="btn" value="免费获取验证码">
<script>
    var wait = 60;
    function time(o){
        if(wait == 0){
            o.removeAttribute("disabled");
            o.value = "免费获取验证码"
            wait = 60;
        }else {
            o.setAttribute("disabled",true);
            o.value = "重新获取("+ wait +")";
            setTimeout(function(){time(o)},500);
            wait--;
        }
    }
    document.getElementById('btn').onclick = function(){time(this);}
</script>
</body>
</html>
