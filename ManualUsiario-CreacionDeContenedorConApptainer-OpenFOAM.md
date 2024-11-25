# Creación de un contenedor con Apptainer y OpenFOAM en la Grid UNAM.
Elaborado por:
Raúl Cruz Martínez.

Prerrequisitos:
- Cuenta de usuario en el nodo submit con autorización para la generación de tokens.
- Acceso al almacenamiento S3.

## Trabajo de HTCondor.
Para enviar un trabajo y ser encolado, se hace mediante un submit file, el cual contiene el archivo con las instrucciones a ejecutar, las especificaciones de cómo se va a ejecutar, los archivos que se van a generar y el número de trabajos a ejecutar.

Para este submit file, se tiene lo siguiente: 
*executable:* el shell script que se da como ejecutable del trabajo
