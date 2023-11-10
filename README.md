<!DOCTYPE html>
<html lang="en">
<head>
    
    <title>MUSIC WEBSITE</title>
    <link rel="stylesheet" href="music.css">
    <link rel="icon" href="./atlogo.jpg">
</head>
<body>
   <div class="container">
    
    <div class="navbar">
        <img src="./images/OIP.jpeg" class="logo">
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Library</a></li>
            <li><a href="#">Specifications</a></li>            
            <li><a href="#">New Release</a></li>            

        </ul>
    </div>
    <div class="content">
        <div class="left-col">
            <h1>GARMI SONG</h1>
        </div>
        <div class="right-col">
            <p>CLick here to listen music</p>
            <img src="./images/play.png" id="icon">
        </div>
    </div>
   </div>
   <audio id="mysong">
    <source src="./images/Garmi(PagalWorld).mp3" type="audio/mp3">
   </audio>
   <script>
    var mysong = document.getElementById("mysong");
    var icon = document.getElementById("icon");
    icon.onclick = function()
    {
        if(mysong.paused){
            mysong.play();
            icon.src = "./images/pause.png"
        }
        else{
            mysong.pause();
            icon.src = "./images/play.png"
        }
    }
   </script>
   <style>
*{
    margin: 0;
    padding: 0;
    font-family: sans-serif;
}
.container{
    height: 100vh;
    width: 100%;
    background-image: url(./images/OIP.jpeg);
    background-size: cover;
    background-position: center;
    position: relative;
    
}
.navbar{
    width: 88%;
    margin: auto;
    padding: 15px 0;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.logo{
    width: 140px;
    cursor: pointer;
}
.navbar ul li{
    list-style: none;
    display: inline-block;
    margin: 0 15px;
    
}
.navbar ul li a{
    text-decoration: none;
    color: #5f5f5f;
    font-size: 15px;
}
.content{
    width: 100%;
    position: absolute;
    top: 30%;
    
}
.left-col{
    margin-left: 6%;
    
}
.left-col h1{
    font-size: 90px;
    color: #fff;
    line-height: 110px;
    float: left;
    
}
.right-col{
     float: right;
     margin-right: 6%;
     margin-top: 120px;
     display: flex;
     align-items: center;
}
.right-col p{
    font-size: 18px;
    color: #5f5f5f;
    font-weight: 400;
    margin-right: 15px;
}
#icon{
    width: 88px;
    cursor: pointer;
}
</style>
   </body>
</html>
