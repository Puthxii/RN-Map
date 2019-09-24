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
   
    


