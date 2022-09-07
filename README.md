# First install dependencies
npm i

# Start on VSC
ionic serve

<!-- Despliegues en las AppStores -->
# CON CAPACITOR
# Creating Splash Screens and Icons
npm i -g cordova-res
cordova-res android --skip-config --copy
# (Si falla lo anterior)
npm uninstall -g cordova-res
npm i -g cordova-res@0.14.0
cordova-res android --skip-config --copy







# CON CORDOVA
# Si el proyecto era inicialmente de capacitor
ionic integrations disable capacitor
# Plataformas
ionic cordova platform add ios
ionic cordova platform add android
# Resources
ionic cordova resources
ionic cordova resources --force
<!-- ---------------------- -->

# Preparations
# Prepare app to run on Android studio
"target": "es6" (tsconfig.json)
Habilitar modo desarrollador
Habilitar "Instalar via USB" (en móvil físico)

# Generate the www folder
ionic build

# Generate the native project, if it does not already exist
  # Install the Capacitor platform package
  # Copy the native platform template into your project
ionic capacitor add android

ionic capacitor build android
# live reload capacitor
ionic capacitor run android --livereload --external