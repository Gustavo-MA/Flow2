# Flow2
Creacion del segundo Flow con NoteRed
flow2-noteRed
Agregando segundo flow con node-red al repositorio 
Introduccion

Se crea un flow que lleva un conteo cada segundo y muestra la hora cada en pantalla
utilizando noteRed

Material Necesario

En esta actividad utilizamos en siguiente material del primer flow1

Ubuntu 20.04
NodeJS
    NPM
    NodeRed
    Nodos Dashboard  

Instrucciones y requisitos previos   (Previamente instalados)

Para que el flow arranque , se deben instalar los siguientes requisitos:

Instalación de NodeJS. Se recomienda tener instalado NodeJS en alguna versión LTS. Al momento de creación de este documento, se usó la versión 16.17.0LTS. Esta instalación debe incluir las Build-Tools para hacer uso de NPM
Instalación de NodeRed. La instalación se realiza por NPM. Al momento de la creación de este contenido, se usó la versión 3.0.2

-sudo apt install curl curl -curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash - sudo apt-get install -y nodejs sudo apt-get install -y bulid -esential sudo npm install -g -unsite-perm node-red node red --version

Instrucciones de preparación del entorno
---------------------------------------------------------------------------
Para ejecutar este flow, es necesario lo siguiente

Arrancar NodeRed con el comando node-red
Clonar el flow1 anteriormente
Exportar el flow1
descargar JSON
Importar flow
Cambiar el nombre  flow1 --> flow2 (Dando doble clic en el titulo)
Agregar un bloque funtion
Modificar orden: time stamp --> funtion  --> debug
Dar doble clic en el bloque funtion poner:

// Lo que está después de “//” son comentarios
// Crea un objeto Date a partir del payload enviado por timestamp
var date = new Date(msg.payload);
// Cambia el payload para que sea una fecha con formato
msg.payload = date.toString();
// Regresa el mensaje para que se envíe al sigueinte nodo
return msg;
despues dar Done.

Dar dible clic en el bloque timestamp
y Modificar el tiempo activiando la opcion:
inject once after  (Activar)
Poner en  "1" seconds, then
Y seleccionar la opcion de intervalo para repetir.

Por ultimo dar por ultimo hace deploy sobre los bloques timestamp y debug
Y presionar el boton de debug para visualizar los mensajes

-----------------------------------------------------------------------

Instrucciones de operación

Para observar el resutlado de este flow, sólo es necesario abrir la pestaña Debug. 


Resultados
![image](https://user-images.githubusercontent.com/111370930/188944728-2697e741-8bb7-47f8-8bdf-e1602db21db3.png)
Se muestra el resultado en el debug de notered, podemos ver la impresion de la fecha y hora de nuestro hostlocal.

A continuación puede verse una vista previa del resultado de este flow. (Se debe exportar el flow)

[
    {
        "id": "66a79683952ae949",
        "type": "inject",
        "z": "791c6205ba61ac70",
        "name": "",
        "props": [
            {
                "p": "payload"
            },
            {
                "p": "topic",
                "vt": "str"
            }
        ],
        "repeat": "1",
        "crontab": "",
        "once": true,
        "onceDelay": "1",
        "topic": "",
        "payload": "",
        "payloadType": "date",
        "x": 90,
        "y": 140,
        "wires": [
            [
                "38f248c6d39200e5"
            ]
        ]
    }
]

Evidencias

Repositorio github: https://github.com/Gustavo-MA/Flow2/blob/main/README.md

Créditos

Desarrollado por Gustavo Medina e-mail: gustavo.medina@uaem.edu.mx
