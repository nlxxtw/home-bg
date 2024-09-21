<template>
  
  <div class="more-content">  
    相遇是一种缘分！ </div>
</br> 
  <div class="more-content"> 
    关注微信公众号：zdDown  </div> 
  </br> 
  <div class="more-content"> 
    资源官网：www.zdDown.icu
</div>
</br>
<div>
<section id="main">
<video id="player" src="http://api.yujn.cn/api/zzxjj.php?wpon=302" controls="controls" width="100%" height="400px"></video>
</section>
</div>
<div style="text-align: center;">
<section id="buttons">
<button id="switch">  </button>
<button id="next1"> </button>
</section>
</div>
<script>
(function (window, document) {
if (top != self) {
window.top.location.replace(self.location.href);
}
var get = function (id) {
return document.getElementById(id);
}
var bind = function (element, event, callback) {
return element.addEventListener(event, callback);
}
var auto = true;
var player = get('player');
var randomm = function () {
player.src = 'http://api.yujn.cn/api/zzxjj.php?wpon=302?_t=' + Math.random();
player.play();
}
bind(get('next1'), 'click', randomm);
bind(player, 'error', function () {
randomm();
});
bind(get('switch'), 'click', function () {
auto = !auto;
this.innerText = '连续: ' + (auto ? '开' : '关');
});
bind(player, 'ended', function () {
if (auto) randomm();
});
})(window, document);</script>
<style>
#switch,#next1{
background: #7F9CCC;
color:#fff;
line-height:40px;
text-align:center;
width:100px;
border:none;
margin:0 6px;
border-radius:6px;
font-weight:bold;
}
</style>

  
</template>

<style lang="scss" scoped>
.more-content {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 20px;
  width: 100%;
  height: 100%;
}
</style>
