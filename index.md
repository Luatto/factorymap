<html>
<head>
<meta charset="utf-8" />
<title>Create and style clusters</title>
<meta name="viewport" content="initial-scale=1,maximum-scale=1,user-scalable=no" />
<script src="https://api.mapbox.com/mapbox-gl-js/v1.9.1/mapbox-gl.js"></script>
<link href="https://api.mapbox.com/mapbox-gl-js/v1.9.1/mapbox-gl.css" rel="stylesheet" />
<style>
	body { margin: 0; padding: 0; }
	#map { position: absolute; top: 0; bottom: 0; width: 100%; }
.mapboxgl-popup-content-wrapper{
    padding-top: 0px;
    margin-right: 0px;
    padding-right: 0px;
	margin-left: 0px;
    padding-left: 0px;
}
.mapboxgl-popup {
margin-top: 0px;

	min-width: 330px;
	min-height: 200px;
	font: 8px/15px 'Open Sans', sans-serif;
	text-color: white;
	border-radius: 0px;
}
.mapboxgl-popup-content {
	background: #c6c8ee; 
    margin-top: 0px;
	padding-top: 0px;
    margin-right: 0px;
    padding-right: 0px;
	margin-left: 0px;
    padding-left: 0px;
	max-height: 260px;
}	


.cluster {
  background-image: url('https://1.bp.blogspot.com/-WlfHJed1Tlc/XqAKCGO1CtI/AAAAAAAAEaE/K6OH_iDzsuszo6m5WhOwIfHT0flqoxOtQCLcBGAsYHQ/s1600/dot40.png');
  background-size: cover;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  cursor: pointer;
}
</style>
</head>
<body>

<div id="map"></div>

<script>
	mapboxgl.accessToken = 'pk.eyJ1IjoibHVjYXNsdWF0IiwiYSI6ImNrOTdiOThodjB0ajQzcGwyczkwZ2Fnc3kifQ.vQ83gWW5CBR3af1_Xzo6Vw';
    var map = new mapboxgl.Map({
        container: 'map',
        style: 'mapbox://styles/mapbox/streets-v10',
        center: [105.820358, 21.054000],
        zoom: 4
    });

    map.on('load', function() {
        // Add a new source from our GeoJSON data and
        // set the 'cluster' option to true. GL-JS will
        // add the point_count property to your source data.
        map.addSource('earthquakes', {
            type: 'geojson',
            // Point to GeoJSON data. This example visualizes all M1.0+ earthquakes
            // from 12/22/15 to 1/21/16 as logged by USGS' Earthquake hazards program.
            data:
                {
"type": "FeatureCollection",
"crs": { "type": "name", "properties": { "name": "urn:ogc:def:crs:OGC:1.3:CRS84" } },
"features": [
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Southern Industrial Park Yen Bai Province<br> 7,1usd/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 104.9418057, 21.6756925, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> L????ng S??n Industrial Park<br> 82USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.5484642, 20.8822227, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> kcn b???c th??ng long<br> 90USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.77810220000001, 21.124536899999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Binh Luc Industry Zone<br> 46USD/sqm/44years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.03811090000001, 20.4753334, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Yen Phong IP<br> 76USD/ m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.0042073, 21.192171699999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Van Trung Industry Zone<br> 75USD/sqm/45years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.1295336, 21.245377000000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Minh Duc Industry Zone<br> 60USD/sqm/50 years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.12901340000001, 20.9161143, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Song Tra Industry Zone<br> 2.5USD/sqm/montn  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.32404990000001, 20.477980200000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu c??ng nghi???p Lai Vu<br> 55USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.39315120000001, 20.9803076, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Pho Noi A Industry Zone<br> 80USD/sqm/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.02551819999999, 20.956930400000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Yen Binh Industry Zone<br> 60USD/sqm/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.90052350000001, 21.430857199999998, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Diem Thuy Industry Zone<br> 48USD/sqm/40years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.891971, 21.474341800000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Dong Van IV Industry Zone<br> 57USD/sqm/50 years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.8955658, 20.638668899999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Nam Th??ng Long Industrial Park<br> 120USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.761769, 21.082578600000002, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> KCN PH?? NGH??A<br> 5 ha  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.7403123, 20.954691400000002, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu c??ng nghi???p L???i D???<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.704435, 20.977982900000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> L???i Y??n Industry zone<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.7182385, 21.022824, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> KCN VSIP<br> 85USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.9762884, 21.077036400000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p ?????i ?????ng<br> 65USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.99809500000001, 21.1052058, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Tr???c ch??nh KCN Ti??n S??n<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.9977748, 21.1257433, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Yen Phong Industrial Zone 2<br> 76USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.95335009999999, 21.204578099999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p Tha??ch Th????t<br> 85USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.6310474, 21.006475699999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Cum C??ng Nghi???p Tr?????ng An X?? An Kh??nh Ho??i ?????c H?? N???i<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.7263128, 20.997368099999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu c??ng nghi???p x?? kim b??nh<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.918595, 20.573345499999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Tay Bac Cu Chi Industrial Zone<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.4840413, 10.9830763, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Dong Nam Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.6210686, 10.969378300000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Tan Phu Trung Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.53524659999999, 10.921779600000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng nghi???p Khai Quang<br> 63USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.6333236, 21.3079027, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Thang Long II<br> 90-95USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.061348, 20.9146848, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Qu??? V?? Industrial Zone<br> 64USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.1133033, 21.153963099999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Pho Noi B Textile and Garment Industrial Park<br> 70- 75USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.0575056, 20.924525800000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> C???m C??ng nghi???p ????ng th???<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.94637419999999, 21.1795911, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> C???m C??ng Nghi???p Ng???c H???i<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.8515451, 20.9132201, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Thanh Oai Industrial Area<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.80114279999999, 20.8720426, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Quang Minh Industrial Zone<br> 120USD/m2/ 50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.77925209999999, 21.1856191, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng nghi???p Nam C???u Ki???n<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.63354959999999, 20.914779200000002, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu c??ng nghi???p B?? Thi???n 1<br> 45USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.6797689, 21.326165199999998, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p Khai S??n Thu???n Th??nh<br> 52USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.05898620000001, 21.036857300000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Ph??c ??i???n Industrial Park<br> 55USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.2040769, 20.930793000000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Phu Hung Industrial Zone<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.9902281, 20.968720600000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng nghi???p Y??n Phong M??? R???ng<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.0005295, 21.2216375, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu c??ng nghi???p an d????ng<br> 65USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.5796113, 20.873230199999998, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Ecological Zone Cuisine Vinh Hung<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.877388, 20.993811000000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Hai Ha Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 107.74881670000001, 21.3657714, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu c??ng nghi???p DEEP C HP II<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.77959730000001, 20.803984700000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Vsip Hai Duong Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.1732444, 20.928766199999998, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Tan Thoi Hiep Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.6307187, 10.8850243, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Binh Chieu Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.7307943, 10.883324200000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Trang Due Industrial Park<br> 60USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.5715707, 20.857410699999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Tan Truong Industrial Zone<br> 54- 57USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.2270607, 20.935504600000002, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Phuc Khanh Industrial Zone<br> 30USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.31265980000001, 20.4414804, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> H???p L??nh Nam S??n Industrial Zone<br> 60USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.0956465, 21.130895200000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng nghi???p Kh??nh Ph??<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.0225859, 20.232081300000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Yen My II Industrial Zone<br> 80usd/m2/50???  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.0435813, 20.877169599999998, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng nghi???p L???c Son<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 107.83702049999999, 11.5188276, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu c??ng nghi???p Ho?? Ph??<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.9702104, 21.234251400000002, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Nam Dinh Vu non-tariff and industrial park (zone 1)<br> 70- 120USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.81154960000001, 20.815795399999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Cai Lan Industrial Zone<br> 60USD/m2/Years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 107.0448962, 20.972393, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Th???y V??n Industrial Park<br> 30USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.3526452, 21.343331200000002, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> KCN B??nh Xuy??n 2<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.67926749999999, 21.303257500000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p N???i Ho??ng<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.1689138, 21.244645500000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> c??ng ti asia khu c??ng nghi????p song kh??<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.1766047, 21.2435002, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p Fugiang V??n Trung<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.144429, 21.250619700000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Chau Son Industrial Park Henan<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.8976869, 20.5196857, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> KHU C??NG NGHI???P B??NH XUY??N<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.65512270000001, 21.280358100000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p ????? S??n<br> 85usd- 97usd/m2/50???  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.7606923, 20.739311900000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p VSIP<br> 80-90USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.702825, 20.904087499999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p Tam Hi???p<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.62446199999999, 21.082094699999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p Ph??c S??n<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.9861619, 20.216262799999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> ????nh Tr??m Industrial Zone<br> 45USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.12694500000001, 21.254740000000002, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> C???m C??ng nghi???p x?? Chi???ng Ch??u<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.0751174, 20.638599899999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng nghi???p L???c Th???nh<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.5967236, 20.4008295, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> C???m C??ng Nghi???p ?????ng H?????ng<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.10126510000001, 20.0962736, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> C???m C??ng Nghi???p ?????ng Phong<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.7322502, 20.320522400000002, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> C???m C??ng nghi???p ?????ng Tu<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.2040454, 20.595583600000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng nghi???p Nguy???n ?????c C???nh<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.3293252, 20.4471621, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu c??ng nghi???p C???u Ngh??n<br> 50USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.4352464, 20.655644899999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Bau Xeo Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 107.0308742, 10.957122099999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Phu My I Industrial Zone<br> 65  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 107.0480556, 10.5905556, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Song May Industrial Zone<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.9540283, 10.9713461, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Honai Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.93857869999999, 10.950114299999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Amata Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.8909948, 10.939308499999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng nghi???p L??? M??n<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.8128851, 19.7817981, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng nghi???p T??y B???c Ga<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.7659269, 19.826537299999998, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu c??ng nghi???p R???ng ????ng<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.1803625, 19.986333900000002, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Hoa Khanh Industrial Zone<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 108.12876249999999, 16.0833431, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> An Don Industrial Zone Danang<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 108.2323111, 16.0777517, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Da Nang Industrial Park (Khu c??ng nghi???p ???? N???ng)<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 108.23718959999999, 16.0775611, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p Ho?? C???m<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 108.18818469999999, 16.004451400000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Hoang Mai Industrial Zone<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.72491960000001, 19.298073500000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu c??ng Nghi???p Tri L???<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.1563747, 18.947284799999998, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Nam Cam Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.6667367, 18.8261182, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p X??m 4 Nghi Ph??<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.67826239999999, 18.7263096, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> C???ng Khu c??ng nghi???p VSIP Ngh??? An<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.6319649, 18.704521700000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu c??ng nghi???p v??ng b???c ???? qu??<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.5986283, 18.689282800000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Bim Son Industrial Park<br> 30USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.8466638, 20.109590399999998, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng nghi???p Ph?? Vinh<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.39840409999999, 18.012982000000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Northwest Industrial Park in Dong Hoi<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.583641, 17.488457199999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu c??ng nghi???p Qu??n Ngang<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 107.08124410000001, 16.8904143, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p Nam ????ng H??<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 107.11366630000001, 16.789783799999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> C???m c??ng nghi???p Di??n Sanh<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 107.2559605, 16.68083, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Dac Loc industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 109.16199109999999, 12.3012961, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Quang Ngai VSIP Industrial Zone<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 108.7892724, 15.215720900000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Tinh Phong Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 108.7988366, 15.1988612, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Quang Phu industrial zone<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 108.7671053, 15.118623400000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p Ph?? T??i<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 109.1448314, 13.782018900000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> An Phuoc Industrial Zone<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.9618341, 10.853688, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Phu An Thanh Industrial Park<br> 119-135,  144-160 USD  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.4516149, 10.6813024, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> KCN Long Duc<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.9785175, 10.842186099999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p Ninh Th???y<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 109.2466924, 12.504872600000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Suoi Dau Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 109.0681374, 12.1487763, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Tan Binh Industrial Zone (Tanimex)<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.623893, 10.8152115, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> An Ha Industrial Zone<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.5109631, 10.811871200000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Tan Tao Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.5902876, 10.7460816, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Le Minh Xuan Industrial Zone<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.54235799999999, 10.7418662, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Phong Phu Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.6433966, 10.6983537, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Hiep Phuoc Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.7466009, 10.638517, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Robustness port Hiep Phuoc Industrial Zone<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.7347827, 10.6528358, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Trung An industrial cluster<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.332888, 10.3476658, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Hoa Phu Industrial Park<br> 60 USD  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.93197480000001, 10.1730071, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Binh Minh Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.82423780000001, 10.037643299999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Chau Duc Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 107.1706398, 10.58925, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Da Bac Industrial Zone<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 107.2757864, 10.5789048, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu c??ng nghi???p ?????t ????? 1<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 107.30223839999999, 10.504759999999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p Long S??n<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 107.08916670000001, 10.452500000000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Dong Xuyen Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 107.11637380000001, 10.399841, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Giao Long Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.4001846, 10.2981146, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Tra Noc Industrial Zone in Can Tho<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.7152609, 10.1006312, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng nghi???p X???o R??<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.11680339999999, 9.8504684000000005, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu CN Kh??nh An<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.0577457, 9.2279234999999993, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p Th???nh L???c<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.13189819999999, 9.9899632999999994, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Binh Long Industrial Zone<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.249289, 10.567171500000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Binh Hoa Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.3418949, 10.4544572, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Song Hau Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.5985542, 10.2499033, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Linh Trung 3 Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.3943622, 11.013886599999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Trang Bang Industrial Zone<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.3949516, 11.0214242, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Bourbon An Hoa TransAsia Industrial Garden (Khu c??ng nghi???p Xuy??n ?? Bourbon An H??a)<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.3278052, 11.034349000000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> KCN Th??nh Th??nh C??ng<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.3192514, 11.021049, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Phuoc Dong Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.3191905, 11.1370942, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu c??ng nghi???p Ch?? L??<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.2058837, 11.295595499999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu c??ng nghi???p Tam Th??ng<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 108.4684354, 15.619972199999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p H??a B??nh<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 107.9891252, 14.3234467, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu c??ng nghi???p Tr?? ??a<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 108.03171, 14.019297, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p ????ng Mai<br> 55usd/m2/50???  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.84121020000001, 21.0060763, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p Thanh B??nh<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.8040965, 21.933755099999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Long Binh Industrial Park - An, Tuyen Quang<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.24653669999999, 21.731650200000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Thai Hoa Industrial Park<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.4744537, 10.9283622, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> C???m c??ng nghi???p B???ch H???c<br> 0,43USD/m2/years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.44409709999999, 21.2832878, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Kcn ?????ng L???ng<br> 25USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.3504611, 21.385528000000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu c??ng nghi???p ?????i An<br> 55-68USD/m2/Years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.2669247, 20.9297632, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> VSIP<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.9653268, 21.0940358, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> ??????????????????<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.77925209999999, 21.1856191, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p Thu???n Th??nh 2<br> 32USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.09585079999999, 21.056609999999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Thuan Thanh III Industrial Park<br> 58USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.0583468, 21.047789999999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Hanaka Industrial Park<br> 39USD/m2/years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.9582372, 21.124624600000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu CN B??nh V??ng<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 104.9768543, 22.713180099999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Dong Van I industrial Zone<br> 50-55USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.9218913, 20.6364418, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Dong Van II Industrial Park<br> 58USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.91757680000001, 20.665318500000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p Vi???t H??a-Kenmark<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.2871315, 20.939228799999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> IZ Lai Cach<br> 55USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.2516315, 20.934606200000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Tien Hai Industrial Park<br> 25USD/m2?50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.52158129999999, 20.391947099999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng nghi???p H???i Y??n - Viglacera<br> 30USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 107.91613630000001, 21.541309800000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Que Vo III Industrial Park<br> 65USD/m2/years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.17879600000001, 21.138383300000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Que Vo Industrial Park 2<br> 64USD/m2/50years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.2220739, 21.128552500000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> KCN Ph?? Th??i<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.51456020000001, 20.962667100000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> KCN C???NG HO?? CH?? LINH H???I D????NG<br> 50USD/m2/years  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.4217838, 21.129179499999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Luong Son Cluster Industrial Zone<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.2952591, 21.401541099999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Tan Hung Cluster Industrial Zone<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.2916431, 21.351537, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Ba Thien II Industrial Zone<br> 70-75usd/sqm  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.6750613, 21.338784499999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu c??ng nghi???p Gia L???<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.35668099999999, 20.503223500000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu C??ng Nghi???p T??n Li??n<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.4915608, 20.703779600000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> KCN H??a x??<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.1461747, 20.417607199999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Khu c??ng nghi???p M??? Trung<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.1930152, 20.452692500000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Bao Minh Industrial Zone Management Board<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.1031586, 20.344221399999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> ?? Y??n II Industrial zone<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.95436340000001, 20.405581999999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Kh??nh Ph?? Industrial Zone<br> 35-40 Usd/sqm/year  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.0303645, 20.244480500000002, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> HANSSIP<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.9147741, 20.708827500000002, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Phu nghia 2<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.671415, 20.929724799999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> KCN Hi???p Ph?????c 2<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.7515861, 10.641088399999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> KCX Linh Trung 1<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.768351, 10.8686091, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> KCN QUANG MINH<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.74798319999999, 21.206851, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> KCN H?? N???I - ????I T??<br> 10 ha  </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.9263243, 21.026779399999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Bien Hoa 2<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.87755249999999, 10.928039399999999, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Cat Lai 2<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.7726538, 10.764358, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> KCN KCX T??N THU???N<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.72983619999999, 10.752447800000001, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> KCX Linh Trung 2<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.7240779, 10.8906212, 105.5 ] } }, 
{ "type": "Feature", "properties": { "id": "ak16994519", "mag": "<div align='center'><a href=# style=text-decoration:none><p align=middle><font size=3> Long H???u<br>   </font></p></a></div>", "time": 1507425289659, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 106.7143665, 10.6385048, 105.5 ] } }, 




{ "type": "Feature", "properties": { "id": "hv61900626", "mag": "<div align='center'><a href=https://sites.google.com/add-group.net/hotels-services/hotel-apartment/google-map/an-binh-city style=text-decoration:none><p align=middle><font size=3> KDTM Nghia Do <br> 33,372,880vnd/sqm  </font></p></a></div>", "time": 1504833891990, "felt": null, "tsunami": 0 }, "geometry": { "type": "Point", "coordinates": [ 105.792779, 21.051467, 2.609 ] } }
]
},
            cluster: true,
            clusterMaxZoom: 14, // Max zoom to cluster points on
            clusterRadius: 50 // Radius of each cluster when clustering points (defaults to 50)
        });

        map.addLayer({
            id: 'clusters',
            type: 'circle',
            source: 'earthquakes',
			style: 'cluster',
            filter: ['has', 'point_count'],
            paint: {
                // Use step expressions (https://docs.mapbox.com/mapbox-gl-js/style-spec/#expressions-step)
                // with three steps to implement three types of circles:
                //   * Blue, 20px circles when point count is less than 100
                //   * Yellow, 30px circles when point count is between 100 and 750
                //   * Pink, 40px circles when point count is greater than or equal to 750
                'circle-color': [
                    'step',
                    ['get', 'point_count'],
                    '#ff7800',
                    100,
                    '#f1f075',
                    750,
                    '#f28cb1'
                ],
				'circle-stroke-color': [
                    'step',
                    ['get', 'point_count'],
                    '#ffae00',
                    100,
                    '#ffae00',
                    750,
                    '#ffae00'
                ],
				'circle-stroke-width': 8,
                'circle-radius': [
                    'step',
                    ['get', 'point_count'],
                    10,
                    100,
                    15,
                    750,
                    20
                ]
            }
        });

        map.addLayer({
            id: 'cluster-count',
            type: 'symbol',
            source: 'earthquakes',
            filter: ['has', 'point_count'],
            layout: {
                'text-field': '{point_count_abbreviated}',
                'text-font': ['DIN Offc Pro Medium', 'Arial Unicode MS Bold'],
                'text-size': 12
            }
        });

        map.addLayer({
            id: 'unclustered-point',
            type: 'circle',
            source: 'earthquakes',
            filter: ['!', ['has', 'point_count']],
            paint: {
                'circle-color': 'Blue',
                'circle-radius': 4,
                'circle-stroke-width': 8,
                'circle-stroke-color': '#7678b5'
            }
        });

        // inspect a cluster on click
        map.on('click', 'clusters', function(e) {
            var features = map.queryRenderedFeatures(e.point, {
                layers: ['clusters']
            });
            var clusterId = features[0].properties.cluster_id;
            map.getSource('earthquakes').getClusterExpansionZoom(
                clusterId,
                function(err, zoom) {
                    if (err) return;

                    map.easeTo({
                        center: features[0].geometry.coordinates,
                        zoom: zoom
                    });
                }
            );
        });
        
        // When a click event occurs on a feature in
        // the unclustered-point layer, open a popup at
        // the location of the feature, with
        // description HTML from its properties.
        map.on('click', 'unclustered-point', function(e) {

            var coordinates = e.features[0].geometry.coordinates.slice();
            var mag = e.features[0].properties.mag;
            new mapboxgl.Popup({className: 'mapboxgl'})
                .setLngLat(coordinates)
                .setHTML("<img src=' https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhG7CLyWYdCqwbQjNnh9mib3izmoGkHVvIOgLqP1f_FYcfffD2BI1FVX48Di0TcV-o0w9CRaZFfgwL4DomY1ybCHKQrTAA86OFpSnit0ukBoVPSm8fRiDEm16GObLBQEAa-U1z5wLJcZy5S7ivyrggaUUVB6TZ4igZ3kjnlJE-SG4DfrSxJ5SMOtKiH/s320/ADD%20Industry.jpg' height='220px' width='330px'>"  + mag )
                .addTo(map);
        });

        map.on('mouseenter', 'clusters', function() {
            map.getCanvas().style.cursor = 'pointer';
        });
        map.on('mouseleave', 'clusters', function() {
            map.getCanvas().style.cursor = '';
        });
    });
</script>

</body>
</html>
