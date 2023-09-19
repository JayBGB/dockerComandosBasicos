# dockerComandosBasicos

## 1. Descargar la imagen Ubuntu y comprobar que está en el equipo.
<details>
<summary>Explicación del primer paso.</summary>

Usamos el comando `docker pull ubuntu` para descargar la imagen de Ubuntu a nuestro ordenador. A continuación, utilizamos `docker images` para comprobar que lo hemos hecho correctamente y que, en efecto, la imagen se ha descargado con éxito.

```bash

docker pull ubuntu

docker images
```
</details>

## 2. Crear un contenedor sin ponerle nombre y comprobar si está arrancado. Después, obtener el nombre.
<details>
<summary>Explicación del segundo paso.</summary>

Utilizo el comando `docker run -dit ubuntu:latest bash` para crear un contenedor con un nombre aleatorio, y posteriormente uso `docker ps` para ver el nombre, que es ***sweet_poitras***.

```bash

docker run -dit ubuntu:latest bash

docker ps
```
</details>

## 3. Crear un contenedor con el nombre 'dam_ubu1'. ¿Cómo se puede acceder a él?
<details>
<summary>Explicación del tercer paso.</summary>

Para crear un contenedor con nombre simplemente hay que añadir *"--name **nombre**"* al comando, quedando así: `docker run -dit --name dam_ubu1 ubuntu:latest bash`.
Para acceder, dado que estoy trabajando con **Visual Studio Code**, puedo usar el menú de Docker integrado en el programa. También podemos acceder con el comando `docker exec -it dam_ubu1 bash`.

```bash

docker run -dit --name dam_ubu1 ubuntu:latest bash

docker exec -it dam_ubu1 bash
```

</details>

## 4. Comprobar qué IP tiene y si se puede hacer un ping a google.com
<details>
<summary>Explicación del cuarto paso.</summary>

Tras llevar a cabo la `apt update` y hacer las instalaciones pertinentes con `apt install net-tools` y `apt install iputils-ping`, utilizamos el comando `ifconfig` para ver la IP del contenedor, que es **172.17.0.3**. Para hacer *ping* a Google, utilizamos `ping google.com` y así se llevará a cabo la acción, que continuará hasta que la finalicemos con **CTRL+C**.

```bash

apt update

apt install net-tools

apt install iputils-ping

ifconfig

ping google.com
```  
</details>

## 5. Crea un contenedor con el nombre 'dam_ubu2'. ¿Puedes hacer ping entre los contenedores?
## 6. Sal del terminal, ¿que ocurrió con el contenedor?
## 7. ¿Cuanta memoria en el disco duro ocupaste?
## 8. ¿Cuanta RAM ocupan los contenedores? ¿Hay algún comando docker para saber esto?.
