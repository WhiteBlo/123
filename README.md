# 123
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
    *{
        margin:0;
        padding: 0;
    }
    div{
       position: relative;
       width: 600px;
       height: 86px;
       margin:50px auto; 
       overflow: hidden;
       border: 2px solid red;
       /*display: flex;
       justify-content:flex-start;
       flex-direction: row;
       flex-wrap: nowrap;*/
    }

    ul{
        list-style: none;
        display: block;
        position: absolute; 
        left: 0;
        top: 0;
    }
    li{
        float:left;
        width: 200px;
    }
   
    </style>
</head>
<body>
    <div id='img'>
      <ul id='ul'>
           <li><img src="images/1x.png"></li>
           <li><img src="images/2x.png"></li>
           <li><img src="images/3x.png"></li>
           <li><img src="images/2x.png"></li>
           <li><img src="images/3x.png"></li>
       </ul>
    </div>   
       
   
   <script>
    var oDiv = document.getElementById('img');
    var oUl = document.getElementById('ul');
    var oImg = document.getElementsByTagName('li');
    var iLeft = 0;
    var timer = null; 
    var iWidth = 200;
    var iTarget = -(iWidth * oImg.length - 600);   
    timer = setInterval(function () {
        iLeft --;
        if (iLeft <= iTarget) {
            clearInterval(timer);
            return;
        }
        oUl.style.left = iLeft + 'px';
    },17);
   </script> 
</body>
</html>