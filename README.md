# 1er Parcial Espacialización en Back End

Examen parcial
Llegamos a la evaluación parcial donde pondremos en práctica todos los conocimientos
vistos hasta el momento, tanto en clase como en Playground. 


# Consigna
A partir de la siguiente arquitectura de microservicios, te pedimos implementar la misma
utilizando Spring Cloud.

![imagen](https://user-images.githubusercontent.com/82984433/187094254-68bd68fe-56e8-434c-aae8-327b06b053e8.png)


Contarás con los microservicios Movie y Catalog. Deberás configurar Eureka server para el
autodescubrimiento de los microservicios, utilizando los nombres:
- movie-service
- catalog-service

A su vez, te pedimos crear el proyecto gateway y configurar el ruteo para ambos
microservicios. También deberás agregar y configurar server config para obtener la
configuración desde un repositorio Git.

Luego, configurar el puerto de cada microservicio desde un repositorio de Git:
- Propiedad:
- server.port=

# movie-service
Es una API REST que nos permite traer las películas por género. El endpoint deberá ser:
/movies/{genre}. Cada película tiene como atributo:
- id
- name
- genre
- urlStream

# catalog-service
API REST que nos permite buscar en el catálogo por género. Por el momento solo
buscaremos películas. El endpoint deberá ser: /catalog/{genre}.

- Utilizar Feign para comunicarnos con el microservicio movie-service y
obtener películas.


La respuesta tiene la siguiente estructura:
- genre
    * movies
        + id
        + name
        + genre
        + urlStream

# Test
Agregar una película de género “Acción” en el microservicio movie y consultar el catálogo
mediante request al endpoint /catalog/{genre} (catalog-service).
