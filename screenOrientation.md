# Ionic Native Screen Orientation 
https://ionicframework.com/docs/native/screen-orientation/

Initially install 
1. ionic cordova plugin add git+https://github.com/apache/cordova-plugin-screen-orientation.git.
2. npm install --save @ionic-native/screen-orientation
3. after installation add app.module.ts
4. import { ScreenOrientation } from '@ionic-native/screen-orientation'; and in provider add "ScreenOrientation"
5. add in app.component.ts
6. this.platform.ready().then(() => {
      // Okay, so the platform is ready and our plugins are available.
      // Here you can do any higher level native things you might need.
      this.statusBar.styleDefault();
      if (this.platform.is('cordova')) {
        this.platform.ready().then(() => {
          this.screenOrientation.lock(this.screenOrientation.ORIENTATIONS.PORTRAIT);
        })
      }
      this.splashScreen.hide();

    });
