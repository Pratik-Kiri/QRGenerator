# QRGenerator
QR Generator Library and Saves the QR Code as Image

### Featured In:
[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-QRGenerator-green.svg?style=true)](https://android-arsenal.com/details/1/3890)
### How to Import the Library:
<b>Gradle:</b>
```groovy
compile 'androidmads.library.qrgenearator:QRGenearator:1.0.3'
```

### Permission:
Add This Permission for saving your generated code
```xml
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"/>
```
### How to use this Library:
After importing this library, use the following lines to use this library.
The following lines are used to generated the QR Code
```java
// Initializing the QR Encoder with your value to be encoded, type you required and Dimension
QRGEncoder qrgEncoder = new QRGEncoder(inputValue, null, QRGContents.Type.TEXT, smallerDimension);
try {
  // Getting QR-Code as Bitmap
  bitmap = qrgEncoder.encodeAsBitmap();
  // Setting Bitmap to ImageView
  qrImage.setImageBitmap(bitmap);
} catch (WriterException e) {
  Log.v(TAG, e.toString());
}
```

Save QR Code as Image 
```java
// Save with location, value, bitmap returned and type of Image(JPG/PNG).
QRGSaver.save(savePath, edtValue.getText().toString().trim(), bitmap, QRGContents.ImageType.IMAGE_JPEG);
```

