# Matriz_PontoObjetivo
Definição da Matriz Ponto Objetivo

<!DOCTYPE html>
<html>
<head>
  <title>Selecionar ponto</title>
  <meta charset="utf-8" />
  <link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css" />
  <style>
    #map { height: 500px; }
  </style>
</head>
<body>

<h3>Clique no ponto de monitoramento</h3>
<div id="map"></div>

<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>
<script>
  var map = L.map('map').setView([-22.5, -44.5], 8);

  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png').addTo(map);

  map.on('click', function(e) {
    var lat = e.latlng.lat;
    var lng = e.latlng.lng;

    // Redireciona para o Google Forms com dados
    window.location.href = "https://docs.google.com/forms/d/e/SEU_FORM_ID/viewform?entry.123=" 
      + lat + "&entry.456=" + lng;
  });
</script>

</body>
</html>
