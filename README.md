# zstore-builder

Workflow réutilisable qui compile les apps envoyées depuis Z-Store.
Ce repo doit s'appeler `zstore-builder` et être **public**. Il ne contient aucun secret : les clés vivent dans les secrets de chaque repo d'app, et c'est le serveur Z-Store qui les y installe.

Étapes :
1. checkout
2. lecture de `.zstore/build.json`
3. Java, Node et Gradle
4. compilation (Gradle ou Capacitor)
5. zipalign et apksigner
6. lecture du package et de la version avec aapt2
7. envoi de l'APK au serveur Z-Store, ou des erreurs en cas d'échec
