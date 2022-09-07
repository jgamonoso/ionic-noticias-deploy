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