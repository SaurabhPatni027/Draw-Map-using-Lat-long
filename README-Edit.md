# Draw-Map-using-Lat-long
basic verison for MAP


<html>
<head>
<title>Show Google Map with Latitude and Longitude Using Jquery Author:SAURABH PATNI</title>
<style type="text/css">
html { height: 100% }
body { height: 100%; margin: 0; padding: 0 }
#map_canvas { height: 100% }
</style>
<script type="text/javascript"
src="https://maps.googleapis.com/maps/api/js?key=AIzaSyC6v5-2uaq_wusHDktM9ILcqIrlPtnZgEk&sensor=false">
</script>
<script type="text/javascript">
function initialize() {
//alert("IN");
var lat = document.getElementById('txtlat').value;
var lon = document.getElementById('txtlon').value;
var myLatlng = new google.maps.LatLng(lat, lon) // This is used to center the map to show our markers
var mapOptions = {
center: myLatlng,
zoom: 6,
mapTypeId: google.maps.MapTypeId.ROADMAP,
marker: true
};
var map = new google.maps.Map(document.getElementById("map_canvas"), mapOptions);
var marker = new google.maps.Marker({
position: myLatlng
});
marker.setMap(map);
}
</script>
</head>
<body >
<form id="form1" runat="server">
<table>
<tr>
<td>Enter Latitude:</td>
<td><input type="text" id="txtlat" value="26.9124" /> </td>
</tr>
<tr>
<td>Enter Longitude:</td>
<td><input type="text" id="txtlon" value="75.7873" /> </td>
</tr>
<tr>
<td></td>
<td><input type="button" value="Submit" onclick="javascript:initialize()" /> </td>
</tr>
</table>
<div id="map_canvas" style="width: 500px; height: 400px"></div>
</form>
</body>
</html>
