# NodejsAlberto

Pasos de instalaci�n de Node.js para notificaciones en firebase:

## Instalamos express:
 
En la consola en nuestro caso de C9 en enviroment:
npm install -g express ( Si queremos que sea accesible a todos)
npm install express ( Para instalaci�n en la propia carpeta)

## Instalamos Firebase:

npm install firebase-admin

## Informaci�n

Al crear un nuevo proyecto en Firebase nos suministra unas credenciales que meteremos en un archivo .json en la carpeta donde hayamos hecho nuestro coneccion.js para iniciar la conexi�n y tenga los permisos.

## C�digo para enlazar

Codido para nuestro .js principal para enlazar con nuestro proyecto del firebase Cloud Messaging y la ruta de donde est�n las credenciales.

var admin = require('firebase-admin');
var serviceAccount = require('./dbfirebase.json');
admin.initializeApp({

    credential: admin.credential.cert(serviceAccount),
    databaseURL: 'https://nombre-proyecto.firebaseio.com'
});
