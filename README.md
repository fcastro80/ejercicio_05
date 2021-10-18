# ejercicio_05

HEALTHCHECK


0 → Significa que el contenedor funcionaría bien y el servicio está correcto.
1 → Este código de retorno significaría que el contenedor no está dando el servicio esperado.

Y es que a partir de Docker 1.12, existe un nuevo concepto en Docker que nos permite indicar como se comprueba la salud de un contenedor. Para hacerlo, solo necesitamos declarar como se verifica si el contenedor está saludable o no, y es tan simple como un comando, que puede devolver:

Este healthcheck puede especificarse en el Dockerfile y en el docker run o docker-compose.yml. En caso de tener varios en el Dockerfile, solo queda activo el último declarado. Si se especifica uno en runtime, este tiene preferencia sobre el que declare la imagen; esto puede servir para sobreescribirlo o deshabilitarlo.



ONBUILD



El comando ONBUIld es usado para especificar el comando que se ejecuta cuando una nueva imagen def docker es usado como base de imagen de otra imagen ( imagen hija ). Se puede usar ONBUILD donde necesita una imagen base con un configuracion dinmaica que cambia en una nueva imagen o se puede usar cuando una imagen depende de otra imagen.



VOLUME


The VOLUME command will specify a mount point in the container. This mount point will be mapped to a location on the host that is either specified when the container is created or if not specified chosen automatically from a directory created in /var/lib/docker/volumes.

If the directory chosen as the mount point contains any files then these files will be copied into this volume. The advantage over mkdir is that it will persist the files to a location on the host machine after the container is terminated.

