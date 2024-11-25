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
*output:* contendrá lo impreso en stdout  
*error:* contendrá lo impreso en stderr  
*log:* contendrá la bitácora del trabajo  
Si se sigue la nomenclatura propuesta, estarán nombrados con el  número de trabajo, el proceso y un sufijo que indica su contenido

*ShouldTransferFiles:* indica que se quiere realizar la transferencia de archivos entre el nodo submit y el worker, y que esta transferencia se realizará en la finalización del trabajo.  
*+xcount:* indica el número de cores que se van a utilizar para la ejecución del trabajo.  
*queue:* indica que el trabajo debe ser encolado.  
