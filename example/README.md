# example

```
import 'package:flutter/material.dart';
import 'package:meet_network_image/meet_network_image.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: Scaffold(
        appBar: AppBar(
          title: Text('MeetNetworkImage example'),
        ),
        body: Container(
          child: SingleChildScrollView(
            child: Column(
              children: <Widget>[
                MeetNetworkImage(
                  height: 200,
                  width: 200,
                  fit: BoxFit.fill,
                  color: Colors.blue,
                  colorBlendMode: BlendMode.difference,
                  imageUrl:
                      "https://random.dog/3f62f2c1-e0cb-4077-8cd9-1ca76bfe98d5.jpg",
                  loadingBuilder: (context) => Center(
                        child: CircularProgressIndicator(),
                      ),
                  errorBuilder: (context, e) => Center(
                        child: Text('Error appear!'),
                      ),
                ),
                MeetNetworkImage(
                  imageUrl:
                      "https://random.dog/3f62f2c1-e0cb-4077-8cd9-1ca76bfe98d5.jpg",
                  loadingBuilder: (context) => Center(
                        child: CircularProgressIndicator(),
                      ),
                  errorBuilder: (context, e) => Center(
                        child: Text('Error appear!'),
                      ),
                ),
                MeetNetworkImage(
                  imageUrl: "asdqwdsadasdaedaedaeadeassda",
                  loadingBuilder: (context) => Center(
                        child: CircularProgressIndicator(),
                      ),
                  errorBuilder: (context, e) => Center(
                        child: Text('Error appear!'),
                      ),
                ),
                SizedBox(
                  height: 100,
                )
              ],
            ),
          ),
        ),
      ),
    );
  }
}

```

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our 
[online documentation](https://flutter.dev/docs), which offers tutorials, 
samples, guidance on mobile development, and a full API reference.
