# README

This is a sample app to reproduce https://github.com/NativeScript/nativescript-angular/issues/1479

### Platform
Android 8.0

### Steps
1. Tap on an item to go to the detailed view
2. Navigate back to the list view
3. The font color of the visited item should change to red, but it doesn't
4. Scroll through the list or click on another item; at some point the app will crash with this error: `There is no entry with key 'org.nativescript.widgets.StackLayout{1f0cc9 V.E...... ........ 0,-119-1080,42}' in the realized views cache for template with key'visited'.`
5. The problem only occurs when `pageTransition="slide"` is used. The app behaves as expected if the slide transition is removed.
