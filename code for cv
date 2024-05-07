import 'package:flutter/material.dart';
import 'package:latlong2/latlong.dart';
import 'package:flutter_map/flutter_map.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Smart Parking App',
      home: MapScreen(),
      debugShowCheckedModeBanner: false,
    );
  }
}

class MapScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    List<LatLng> parkingLocations = [
      LatLng(11.0176, 76.9674),
      LatLng(10.9902, 76.9629),
      LatLng(11.0102, 76.9504),
      LatLng(11.0269, 76.9058),
      LatLng(11.0171, 76.9853),
      LatLng(11.0238, 76.9452),
      LatLng(10.9991, 76.9773),
      LatLng(11.0118, 76.9615),
      LatLng(10.9974, 76.9585),
      LatLng(11.0232, 76.9608),
      LatLng(11.0556, 76.9939),
      LatLng(11.0304, 77.0391),
      LatLng(11.0463, 76.9471),
      LatLng(11.0271, 76.9830),
      LatLng(11.0304, 77.0391),
    ];

    return Scaffold(
      appBar: AppBar(
        title: Text('Parking Map - Coimbatore'),
      ),
      body: FlutterMap(
        options: MapOptions(
          center: LatLng(11.0168, 76.9558),
          zoom: 13.0,
        ),
        layers: [
          TileLayerOptions(
            urlTemplate: "https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",
            subdomains: ['a', 'b', 'c'],
          ),
          MarkerLayerOptions(
            markers: parkingLocations
                .map(
                  (location) => Marker(
                    width: 80.0,
                    height: 80.0,
                    point: location,
                    builder: (ctx) => Container(
                      child: Column(
                        children: [
                          Icon(
                            Icons.local_parking,
                            color: Colors.green,
                            size: 40.0,
                          ),
                          // Text(
                          //   'P',
                          //   style: TextStyle(
                          //     fontSize: 20.0,
                          //     color: Colors.green,
                          //     fontWeight: FontWeight.bold,
                          //   ),
                          // ),
                        ],
                      ),
                    ),
                  ),
                )
                .toList(),
          ),
        ],
      ),
    );
  }
}
