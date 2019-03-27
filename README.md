# NodejsAlberto

Pasos de instalación de Node.js para notificaciones en firebase:

## Instalamos express:
 
En la consola en nuestro caso de C9 en enviroment:
npm install -g express ( Si queremos que sea accesible a todos)
npm install express ( Para instalación en la propia carpeta)

## Instalamos Firebase:

npm install firebase-admin

## Información

Al crear un nuevo proyecto en Firebase nos suministra unas credenciales que meteremos en un archivo .json en la carpeta donde hayamos hecho nuestro coneccion.js para iniciar la conexión y tenga los permisos.

## Código para enlazar

Codido para nuestro .js principal para enlazar con nuestro proyecto del firebase Cloud Messaging y la ruta de donde estén las credenciales.

var admin = require('firebase-admin');
var serviceAccount = require('./dbfirebase.json');
admin.initializeApp({

    credential: admin.credential.cert(serviceAccount),
    databaseURL: 'https://nombre-proyecto.firebaseio.com'
});
