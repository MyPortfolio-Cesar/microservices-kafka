# Microservice Transaction :smiley:

El proyecto se centra en la gestión de transacciones financieras a través de microservicios. Hemos diseñado dos microservicios principales utilizando Node.js y TypeScript. El primero actúa como una REST API encargada de crear nuevas transacciones, mientras que el segundo se especializa en validar estas transacciones, asegurando que el monto no exceda un límite predeterminado, en nuestro caso, 1000 PEN (unidad monetaria elegida).

# Tecnologías Usadas

<ol>
  <ul><strong>Node.js y TypeScript</strong>: Node.js proporciona un entorno de ejecución de JavaScript del lado del servidor, mientras que TypeScript añade tipado estático para un desarrollo más seguro y mantenible.</ul>
  <ul><strong>MongoDB</strong>: Utilizamos MongoDB como nuestra base de datos para almacenar las transacciones. Su flexibilidad y escalabilidad lo convierten en una elección ideal para aplicaciones modernas.</ul>
  <ul><strong>Kafka</strong>: Implementamos Kafka como un sistema de mensajería para la comunicación entre nuestros microservicios. Esta tecnología nos permite construir una arquitectura de eventos robusta y tolerante a fallos.</ul>
  <ul><strong>Docker Compose</strong>: Para facilitar el despliegue y la gestión de nuestro entorno de desarrollo en diferentes sistemas, utilizamos Docker Compose. Esta herramienta nos permite definir y ejecutar múltiples contenedores de manera eficiente.</ul>

</ol>





# Diagrama de Aplicaciones

![Diagrama de Aplicaciones](https://github.com/MyPortfolio-Cesar/microservices-kafka/blob/master/assets/Diagrama%20de%20aplicaciones.png)


# Requerimientos Previos:

Para poder ejecutar y ver los logs del proyecto, recomiendo descargar **Docker Desktop** para tener una interfaz gráfica mas intuitiva de como se estan manejando los contenedores y ver los logs del sistema.

Link de la página oficial de Docker Desktop para poder descargarlo: https://www.docker.com/products/docker-desktop/

No olvides tener los puertos **3001** y **3002** libres para poder ejecutar los microservicios.

# Instalación y Ejecución

Para poder ejecutar la aplicación debe ubicar en la ruta raiz del proyecto y ejecutar en la consola el siguiente comando: `docker-compose up -d`. De esta forma se empezaran a iniciar en segundo plano los contenedores definidos en el archivo **docker-compose.yml**.

![Docker containers](https://github.com/MyPortfolio-Cesar/microservices-kafka/blob/master/assets/Docker%20containers.png)

![Microservicio Api](https://github.com/MyPortfolio-Cesar/microservices-kafka/blob/master/assets/Microservice%20API.png)

![Microservicio Validator](https://github.com/MyPortfolio-Cesar/microservices-kafka/blob/master/assets/Microservice%20Validator.png)



**NOTA:** Para poder entrar como cliente, se hace uso de Swagger donde esta documentado el API REST y así poder crear transacciones de manera manual.

Swagger se encuentra ubicado en `http://localhost:3001/documentation/`.

![Swagger](https://github.com/MyPortfolio-Cesar/microservices-kafka/blob/master/assets/Swagger%20API%20REST.png)

# Observaciones

- Elegí usar Mongoose en lugar de TypeORM principalmente debido a mi familiaridad y experiencia previa con el ecosistema de MongoDB y Node.js. Mongoose me proporciona una interfaz intuitiva y orientada a objetos para interactuar con MongoDB, lo que me resulta cómodo y eficiente. Aunque tambien tengo conocimientos de TypeORM y conozco sus ventajas, como su soporte para múltiples bases de datos relacionales, decidí utilizar Mongoose en mi proyecto.






