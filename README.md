# prize
###这是一个抽奖系统，主要是为了练习鼠标点击事件和添加键盘事件。<br/>
###封装了一个通过class类名来获取对象的一个函数 getElementsByClass();因为HTML DOM 的getElementsByClassName()方法不支持ie9以下版本。<br/>
###<b>抽奖小程序的基本思路:</b>
<ol>
  <li>定义一个存放抽奖信息的数组arr，计算数组长度len</li>
  <li>通过Math.random()来获取随机数，由于获取的是0-1之间的浮点数，所以需要使用var random = Math.floor(Math.random()*len);来获取随机数random</li>
  <li>点击开始方法：定义一个计时器setInterval()，每隔一定时间，就把获取的arr数组中的元素插入到显示区中</li>
  <li>点击结束：使用clearInterval()清除timer</li>
  <li>添加键盘事件，比如按回车键来控制开始和结束，需要定义一个参数flag。初始默认为flag=false;表示未按回车键开始。</li>
  <li>按回车键开始的时候,触发定时器，设置flag=true表示已经按了回车键开始抽奖了。</li>
  <li>再次按回车键停止抽奖的时候，清除定时器，设置flag=false表示停止</li>
</ol>

###<b>关于键盘事件</b>
  <ol>
    <li>keyDown当用户按下键盘上的任意键时触发，而且如果按住不放的话，会重复触发此事件</li>
    <li>keyPress当用户按下键盘上的字符键时触发。且如果按住不放的话，会重复触发此事件</li>
    <li>keyUp当用户释放键盘上的键时触发</li>
    <li>keycode键码，键盘上的按键对应的数字</li>
  </ol>
  
  ###具体见代码
