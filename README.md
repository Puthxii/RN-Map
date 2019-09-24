# React Native Map Example

### How to Create React Native App
    1. npm install -g react-native-cli 
    2. react-native init RN-Map
    3. cd RN-Map
    4. react-native run-android

### For React Native Version<0.60
    1. react-native link react-native-maps
    
### Generate the API Key
    1. Get API from https://cloud.google.com/maps-platform/pricing/sheet/
    get start
#### ![Alt text](https://www.img.in.th/images/1ff7f66d28f988bd7499c0dcbab4cabb.png)
    pick product
#### ![Alt text](https://www.img.in.th/images/fc45d0f298987866dd536a2999fdf481.png)
    select project 
#### ![Alt text](https://www.img.in.th/images/b19984053666c2ab6ca3e7a45bebf2e7.png)
    click Credential
#### ![Alt text](https://www.img.in.th/images/4f36f57e5ad446df90d9bf0190c6fdcb.png)
    get API Ket
#### ![Alt text](https://www.img.in.th/images/25533709b3892e99a581033def5ca7c6.png)   

### After enabling the API key, we have to add this API key to our project’s AndroidManifest.xml file. Just copy the following lines and paste it into your manifest file with your generated API key.

       <meta-data
          android:name="com.google.android.geo.API_KEY"
          android:value="Replace this with your API key"/>
 
 #### ![Alt text](https://www.img.in.th/images/187cd981eb53a312cd502f9acfa47177.png)   

       
### App.js

        /*This is an Example of React Native Map*/
        import React from 'react';
        import { StyleSheet, Text, View , TextInput} from 'react-native';
        import MapView, {Marker} from 'react-native-maps';

        export default class App extends React.Component {
          onRegionChange(region) {
            this.setState({ region });
          }
          render() {
            var mapStyle=[{"elementType": "geometry", "stylers": [{"color": "#242f3e"}]},{"elementType": "labels.text.fill","stylers": [{"color": "#746855"}]},{"elementType": "labels.text.stroke","stylers": [{"color": "#242f3e"}]},{"featureType": "administrative.locality","elementType": "labels.text.fill","stylers": [{"color": "#d59563"}]},{"featureType": "poi","elementType": "labels.text.fill","stylers": [{"color": "#d59563"}]},{"featureType": "poi.park","elementType": "geometry","stylers": [{"color": "#263c3f"}]},{"featureType": "poi.park","elementType": "labels.text.fill","stylers": [{"color": "#6b9a76"}]},{"featureType": "road","elementType": "geometry","stylers": [{"color": "#38414e"}]},{"featureType": "road","elementType": "geometry.stroke","stylers": [{"color": "#212a37"}]},{"featureType": "road","elementType": "labels.text.fill","stylers": [{"color": "#9ca5b3"}]},{"featureType": "road.highway","elementType": "geometry","stylers": [{"color": "#746855"}]},{"featureType": "road.highway","elementType": "geometry.stroke","stylers": [{"color": "#1f2835"}]},{"featureType": "road.highway","elementType": "labels.text.fill","stylers": [{"color": "#f3d19c"}]},{"featureType": "transit","elementType": "geometry","stylers": [{"color": "#2f3948"}]},{"featureType": "transit.station","elementType": "labels.text.fill","stylers": [{"color": "#d59563"}]},{"featureType": "water","elementType": "geometry","stylers": [{"color": "#17263c"}]},{"featureType": "water","elementType": "labels.text.fill","stylers": [{"color": "#515c6d"}]},{"featureType": "water","elementType": "labels.text.stroke","stylers": [{"color": "#17263c"}]}];
            return (
              <View style={styles.container}>
                <MapView
                  style={styles.map}
                  initialRegion={{
                    latitude: 37.78825,
                    longitude: -122.4324,
                    latitudeDelta: 0.0922,
                    longitudeDelta: 0.0421,
                  }}
                  customMapStyle={mapStyle}
                >
                  <Marker
                    draggable
                    coordinate={{
                      latitude: 37.78825,
                      longitude: -122.4324,
                    }}
                    onDragEnd={(e) => alert(JSON.stringify(e.nativeEvent.coordinate))}
                    title={'Test Marker'}
                    description={'This is a description of the marker'}
                  />
                </MapView>
              </View>
            );
          }
        }

        const styles = StyleSheet.create({
          container: {
            position:'absolute',
            top:0,
            left:0,
            right:0,
            bottom:0,
            alignItems: 'center',
            justifyContent: 'flex-end',
          },
          map: {
            position:'absolute',
            top:0,
            left:0,
            right:0,
            bottom:0,
          },
        });

### Run
    1. cd RN-Map
    2. react-native run-android
    

