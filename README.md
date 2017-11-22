## KC-Modulo-de-DevOps

### Plataforma de alojamiento

La soluciones están alojadas en la plataforma AWS ("Amazon Web Services") y en el dominio *joselinuxalonso.es*. 

### Páginas desplegadas

En el dominio indicado se ha desplegado la página *Nodepop*, correspondiente a la práctica del módulo de módulo de Node.js básico. El repositorio de dicha práctica está en https://github.com/josealonso/KC-Modulo-de-Nodejs_Basico.

En caso de acceder indicando la dirección IP del servidor, que es *54.205.213.229*, se muestra el contenido de la práctica del módulo de fundamentos de HTML. Es mi currículum y el repositorio está en https://github.com/josealonso/KC-Modulo-de-HTML5_CSS3_y_JS 

### Arquitectura usada

- Se ha usado *node* como servidor de aplicación y *PM2* como gestor de procesos de node para que la aplicación Nodepop, que está hecha en Express, esté siempre  en ejecución. 
- Se ha usado *nginx* como *proxy inverso* que se encarga de recibir las peticiones HTTP y derivárselas a node.
- Los archivos estáticos de la aplicación (imágenes y ficheros .css) son servidos por nginx (no por node). Para estos archivos, se ha añadido una cabecera HTTP llamada "X-Owner" (la X- indica que es una *cabecera personalizada*) y cuyo valor es el nombre de mi cuenta de usuario en github.

### HTTPS (HTTP seguro)

Se accede a la aplicación Nodepop mediante una *conexión segura*, también llamada *https*.
Para generar los certificados SSL, se han usado las herramientas gratuitas *letsencrypt* y *certbot*.

### Docker

Siguiendo la documentación oficial de *Docker*, se ha instalado dicha herramienta en la máquina de producción.

