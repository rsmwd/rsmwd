#<!doctype html>
<html>
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>price list test code</title>
</head>

<body>

<div class="wrap">
<div class="tab_container">
  <input id="tab1" type="radio" name="tab_item" checked>
  <label class="tab_item" for="tab1">お悩み別メニュー</label>
  <input id="tab2" type="radio" name="tab_item">
  <label class="tab_item" for="tab2">治療法別メニュー</label>
 
  <div class="tab_content" id="tab1_content">
    <div class="tab_content_description">
      <p class="c-txtsp"><div class="section">
 
  <form>
    <select class="link_menu">
     
      <option value="#pb1">医療レーザー脱毛</option>
      <option value="#pb2">シミ</option>
      <option value="#pb3">シワ</option>
    </select>
  </form>
  <h3 id="pb1" class="oneArea">医療レーザー脱毛メニュー表</h3>
  <h3 id="pb2" class="oneArea">シミメニュー表</h3>
  <h3 id="pb3" class="oneArea">シワメニュー表</h3>
 
</div></p>
    </div>
  </div>
  <div class="tab_content" id="tab2_content">
    <div class="tab_content_description">
      <p class="c-txtsp"><div class="section">
 
  <form>
    <select class="link_menu">
   
      <option value="#treatment1">医療レーザー脱毛</option>
      <option value="#treatment2">メンズ医療レーザー脱毛</option>
      <option value="#treatment3">ピコレーザー</option>
    </select>
  </form>
  <h3 id="treatment1" class="oneArea">医療レーザー脱毛</h3>
  <h3 id="treatment2" class="oneArea">メンズ医療レーザー脱毛</h3>
  <h3 id="treatment3" class="oneArea">ピコレーザー</h3>
 
</div></p>
    </div>
  </div>
  
  
</div>




</div>

<style>

.wrap{
padding-right: 15px;
    padding-left: 15px;
    margin-right: auto;
    margin-left: auto;
	max-width:1200px;
	}

form {
  margin-bottom: 50px;
}
form .link_menu {
  width: 100%;
  padding: 20px;
  font-size: 16px;
  cursor: pointer;
}
h3.oneArea {
  margin-bottom: 1000px;
}


.tab_container {
  padding-bottom: 1em;
  background-color: #fff;
  border:1px solid #D50080;
  margin: 0 auto;}
.tab_item {
  width: calc(100%/2);
  padding:15px 0;
  border-bottom: 3px solid #D50080 ;
  background-color: #ececec;
  text-align: center;
  color: #D50080 ;
  display: block;
  float: left;
  text-align: center;
  font-weight: bold;
  transition: all 0.2s ease;
}
.tab_item:hover {
  opacity: 0.75;
}
input[name="tab_item"] {
  display: none;
}
.tab_content {
  display: none;
  padding: 1em 1em 0;
  clear: both;
  overflow: hidden;
}
#tab1:checked ~ #tab1_content,
#tab2:checked ~ #tab2_content,
#tab3:checked ~ #tab3_content,
#tab4:checked ~ #tab4_content {
  display: block;
}
.tab_container input:checked + .tab_item {
  background-color: #D50080 ;
  color: #fff;
}
</style>

<script src="https://code.jquery.com/jquery-3.2.1.min.js"></script>

<script>$(function () {
  $('select').change(function () {
    var speed = 400;
    var href = $(this).val();
    var target = $(href == "#" || href == "" ? 'html' : href);
    var position = target.offset().top;
    $('body,html').animate({scrollTop:position}, speed, 'swing');
    return false;
  });
});</script>
</body>
</html>
