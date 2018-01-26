# Flutter Advanced Network Imageprovider

[![pub package](https://img.shields.io/pub/v/flutter_advanced_networkimage.svg)](https://pub.dartlang.org/packages/flutter_advanced_networkimage)

An advanced image provider provides caching and retrying for flutter app.

## Getting Started

### Installation
Add this to your pubspec.yaml (or create it):
```yaml
dependencies:
  advanced_imageprovider: any
```
Then run the flutter tooling:
```bash
flutter packages get
```

### Example
```dart
// using image provider
new Image(
  image: new AdvancedNetworkImage(url, header: header, useDiskCache: true),
  fit: BoxFit.cover,
)
```
```dart
// get the disk cache folder size
bool isSucceed = await getDiskCachedImagesSize();
```
```dart
// clean the disk cache
int folderSize = await clearDiskCachedImages();
```
```dart
// using zooming widget
new ZoomableWidget(
  minScale: 0.3,
  maxScale: 2.0,
  child: new Container(...),
)
```

Details in [example/](https://github.com/mchome/flutter_advanced_networkimage/tree/master/example) folder.

## Q&A
- Q: Why the cached files stored in documents directory instead of temporary directory?  
  A: I think your cached fils should be a part of your app, and you can manual clear your cached files.

- Q: Your zooming widget is weird while scrolling, will you improve it?  
  A: Ummmmm, maybe.