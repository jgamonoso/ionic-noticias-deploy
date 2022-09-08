# First install dependencies
npm i

# Start on VSC
ionic serve

<!-- Despliegues en las AppStores -->
# CON CORDOVA
# Si el proyecto era inicialmente de capacitor
ionic integrations disable capacitor
# Plataformas
<!-- ionic cordova platform add ios -->
ionic cordova platform add android
# Luego
npm i -g cordova-res
# Resources
<!-- ionic cordova resources -->
<!-- ionic cordova resources --force -->
ionic cordova resources android --force

# Para generar el build y levantarlo en Android Studio
ionic cordova build android
<!-- D:\Proyectos\IONIC\16-ionic-noticias-deploy-cordova\platforms\android\app\build\outputs\apk\debug\app-debug.apk -->
# Si esto da error de ejecución de Java, borrar la carpeta Android dentro de platforms
# Luego abrir Android Studio
# Para que android studio pille los cambios
Sync project with gradle files

# Generar release de producción (sin firmar)
ionic cordova build android --prod --release
<!-- D:\Proyectos\IONIC\16-ionic-noticias-deploy-cordova\platforms\android\app\build\outputs\bundle\release\app-release.aab -->
# Generar release de producción (sin firmar - apk)
ionic cordova build android --prod --release -- -- --packageType=apk
<!-- D:\Proyectos\IONIC\16-ionic-noticias-deploy-cordova\platforms\android\app\build\outputs\apk\release\app-release-unsigned.apk -->


# Generar+Firmar un APK - Android Studio
<!-- https://developer.android.com/studio/publish/app-signing?hl=es-419#sign_release -->
Build -> Generate signed bundle/apk -> APK
<!-- D:\Proyectos\IONIC\16-ionic-noticias-deploy-cordova\platforms\android\app\release\app-release.apk -->