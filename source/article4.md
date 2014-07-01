## [PhoneGap] Google Map (作者：廖憲得 0xde)

### 大整數加法

```html
<!DOCTYPE html>
<html>
<head>

<meta http-equiv="content-type" content="text/html; charset=UTF-8" />

<script
src="http://maps.googleapis.com/maps/api/js?key=AIzaSyDY0kkJiTPVd2U7aTOAwhc9ySH6oHxOIYM&sensor=false">
</script>

<script>
var map;
function initialize()
{
var mapOpt = {
	center:new google.maps.LatLng(24.150026,120.683868),
	zoom:15,
	mapTypeId:google.maps.MapTypeId.ROADMAP,
	mapTypeControl: false,
	navigationControl : false,
	scaleControl : false,
	streetViewControl: false
  };
map=new google.maps.Map(document.getElementById("googleMap"),mapOpt);
}

function Reinitialize(MapX,MapY)
{
var mapOpt = {
	center:new google.maps.LatLng(MapX,MapY),
	zoom:15,
	mapTypeId:google.maps.MapTypeId.ROADMAP,
	mapTypeControl: false,
	navigationControl : false,
	scaleControl : false,
	streetViewControl: false
  };
map=new google.maps.Map(document.getElementById("googleMap"),mapOpt);
}

google.maps.event.addDomListener(window, 'load',initialize);

</script>
</head>
<body>

<button onclick="map.setMapTypeId(google.maps.MapTypeId.ROADMAP);">道路地圖</button>
<button onclick="map.setMapTypeId(google.maps.MapTypeId.SATELLITE);">衛星地圖</button>
<button onclick="map.setMapTypeId(google.maps.MapTypeId.HYBRID);">混合地圖</button>
<button onclick="map.setMapTypeId(google.maps.MapTypeId.TERRAIN);">實際地圖</button>




	請輸入經緯度：
	<input id="XX" type="text" style="width:80px" >
	<input ID="YY" type="text" style="width:80px" >
	<button onclick="Reinitialize(XX.value,YY.value)">搜尋經緯度</button>

<div id="googleMap" style="width:400px;height:300px;"></div>

</body>
</html>
```

![](../img/PhoneGapGoogleMap.jpg)

【本文作者為「廖憲得」，原文網址為： <http://www.dotblogs.com.tw/0xde/archive/2014/06/27/145727.aspx> ，由陳鍾誠編輯後納入本雜誌】
