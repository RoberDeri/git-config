
  
# Instalación y configuracín de Git en Linux
Git es un sistema de control de versiones muy popular que se usa para poder insertar modificaciones, acceder a registros anteriores y dividir en ramas alternativas el código fuente de un software en desarrollo. Este se guarda en repositorios (como Github y Gitlab) para facilitar la colaboración con otros trabajadores/usuarios del mismo.
## Pasos previos
Necesitará un servidor Ubuntu 20.04 con una cuenta de súper-usuario no root. Una vez que tenga el servidor y el usuario configurados, estará listo para comenzar. Tambien hay que verificar que Git no esté instalado ya en tu equipo. Compruebe con el siguiente comando:<br>
```
git --version
```
En caso de no encontrarse, la terminal informará de su ausencia y sugerirá un comando de instalación.<br>

## Instalación de Git con paquetes predeterminados

Primero actualice el índice local de paquetes:
```
sudo apt update
```
Terminada las actualizaciones, puede comenzar la descarga de Git:

```
sudo apt install git
```
Cuando se termine la instalación debería mostrar un resultado similar a este:

```
git version 2.25.1
```
## Instalar versiones más recientes
En el momento de escribir este documento la última versión es la 2.33.1. Desde el [sitio web de Git] (https://git-scm.com/download/linux) puedes conseguir la PPA (Personal Package Archive) de la última versión estable de Git. Las PPA son muy útiles pues permite estar siempre actualizado en un paquete/software concreto.<br>
Para ello, en Ubuntu ejecute el siguiente código en terminal:
```
add-apt-repository ppa:git-core/ppa
```
Se descargaran una serie de paquetes que para hacerlos efectivos se deben actualizar con:
```
sudo apt update
```
Hecho esto, salga de la terminal y active las actualizaciones que estén pendiente en su aplicación de Actualización de Software. Vuelva a la terminal y compruebe la versión de Git. Debería salir esto: 
```
git version 2.33.1.
```
## Configuración de Git
Lo primero que debe hacer cuando instale Git es establecer su nombre de usuario y dirección de correo electrónico. Esto es importante porque los "commits" de Git usan esta información y es introducida en los commits que envía. Aplique esta información con los siguientes comandos:
```
git config --global user.name "Your Name"
git config --global user.email "youremail@domain.com"
```
Puede ver la información introducida escribiendo:
```
git config --list
```
La información se puede modificar con su editor de texto. En caso de usar Nano, serían los siguientes comandos:
```
nano ~/.gitconfig
```
```
~/.gitconfig contents
[user]
  name = Your Name
  email = youremail@domain.com 
```






  
  
  
  



