mapboxgl.accessToken = 'pk.eyJ1Ijoic2hhZG93bSIsImEiOiJjamJjdXIzcGgxdWQ0MnJwZTFsYXIzbjNjIn0.OQm9we8GDRMDJ-dii6OhZg';

var map = new mapboxgl.Map({
    container: "map",
    style: "mapbox://styles/mapbox/light-v9",
    center: [-73.985130, 40.758896],
    zoom: 11
});


map.on("load", function() {

  var arr=[];



  d3.csv("sample_merged_1.csv", function(data) {
    for (var i = 0; i < 2; i++) {
      var id_taxi;
        id_taxi=data[i].id_taxi;
      var pickup_long;
        pickup_long=data[i].pickup_long;
      var pickup_lat;
        pickup_lat=data[i].pickup_lat;
      var dropoff_long;
        dropoff_long=data[i].dropoff_long;
      var dropoff_lat;
        dropoff_lat=data[i].dropoff_lat;


        map.addSource("pickUpPoints", {
            "type": "geojson",
            "data": {
                "type": "FeatureCollection",
                "features": [
                    {
                        "type": "Feature",
                        "geometry": {
                            "type": "Point",
                            "coordinates": [pickup_long, pickup_lat]
                        }
                    }
              ]
            }
        });
        // map.addLayer({
        //     "id": id_taxi,  "type": "circle", "source": "pickUpPoints",
        //     "paint": {
        //         "circle-radius": 2.5, "circle-color": "#B42222"
        //     },
        //     // "filter": ["==", "$type", "Point"],
        // });

    };

  });


    // map.addSource("pickUpPoints", {
    //     "type": "geojson",
    //     "data": {
    //         "type": "FeatureCollection",
    //         "features": [
    //             {
    //                 "type": "Feature",
    //                 "geometry": {
    //                     "type": "Point",
    //                     "coordinates": [-73.985130, 40.738896]
    //                 }
    //             }
    //       ]
    //     }
    // });
    // map.addSource("DropOffPoints", {
    //     "type": "geojson",
    //     "data": {
    //         "type": "FeatureCollection",
    //         "features": [
    //             {
    //                 "type": "Feature",
    //                 "geometry": {
    //                     "type": "Point",
    //                     "coordinates":[-73.989130, 40.768896]
    //                 }
    //             }
    //       ]
    //     }
    // });


    //
    // map.addLayer({
    //     "id": "dropPoint",  "type": "circle", "source": "DropOffPoints",
    //     "paint": {
    //         "circle-radius": 2.5, "circle-color": "#009E1F"
    //     },
    //     "filter": ["==", "$type", "Point"],
    // });


});
