# ejercicio_05

HEALTHCHECK

A partir de Docker 1.12, existe un nuevo concepto en Docker que nos permite indicar como se comprueba la salud de un contenedor. Este comando puede devolver:

0 → Significa que el contenedor funcionaría bien y el servicio está correcto.
1 → Este código de retorno significaría que el contenedor no está dando el servicio esperado.


Este healthcheck puede especificarse en el Dockerfile y en el docker run o docker-compose.yml. En caso de tener varios en el Dockerfile, solo queda activo el último declarado. Si se especifica uno en runtime, este tiene preferencia sobre el que declare la imagen; esto puede servir para sobreescribirlo o deshabilitarlo.



ONBUILD

El comando ONBUILD es usado para especificar el comando que se ejecuta cuando una nueva imagen de docker es usado como  imagen base de otra imagen ( imagen hija ). Se puede usar ONBUILD por ej en una imagen base con un configuracion dinamica que cambia en una nueva imagen o se puede usar cuando una imagen dependa de otra imagen.



VOLUME

Este comando especifica el punto de montaje en el contendor. Este punto de montaje sera mapeado a la ubicacion en el host que es creado o sino se especifica automaticamente en el directorio creado en /var/lib/docker/volumes

Si el directorio escogido como punto de montaje contiene algun archivo, entonces estos son copiados en dicho volumen. 

