# Pasos para crear una pagina en Jekyll

Con este tutorial enseñaremos paso a paso a como instalar una pagina en GitHub Pages basado en un generador de paginas web estaticas llamado Jekyll

## Requisitos

Para empezar deberemos tener:
- Un editor de codigo, puede ser cualquiera pero recomiendo Visual Studio Code. 
- Una maquina virtual Linux (Ubuntu, Debian, etc) con servicios de Git para instalar el Jekyll en el y todos sus recursos.
  
Nos pondremos en Visual Studio, teniendo la extension de SSH instalada, nos meteremos a la maquina virtual presionando **F1** y escribiendo:

>remote-ssh:Connect to host

Ahi nos pedira la IP de la maquina asi que la pondremos y damos a enter para que se nos abra otra pagina y ahi nos saldran varias opciones de sistemas operativos, elegimos **Linux** y ahi nos habra conectado con la maquina virtual.

## Paso 1 Instalaciones Previas

Para comenzar abriremos un terminal en el Visual Studio Code conectado a la maquina virtual, y ahi nos aseguramos de que este actualizado con *"sudo apt update -y"* y luego aplicando con *"sudo apt upgrade"* pero eso es para asegurarse.

Despues instalaremos los paquetes "RubyGems" o "Gemas" con el usuario root, lo haremos escribiendo esta linea de comandos:

```
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc

gem install jekyll bundler

```

## Paso 2 Creacion de un repositorio

En nuestro GitHub deberemos de crear un nuevo repositorio. Para ello tendremos que tener una cuenta en GitHub creada y a continuacion, deberemos de darle a "New" que esta nada mas entrar en la pagina de inicio a la izquierda.

De nombre le ponemos el que sea.

Despues dentro de la maquina virtual, habra que hacer un directorio el cual se correspondera con el repositorio

> mkdir [nombre_que_sea]

Nos metemos al directorio

> cd [nombre_que_sea]

Y una vez aqui haremos un *"git init"* para inicializar el repositorio y luego *"git remote add origin https://[Nombre_usuario]:[Token]@[direccion_del_repositorio]"*

## Paso 3 Hacer el sitio Jekyll

Una vez echo haremos un cambio de ramas con *"git checkout -b gh-pages"* que tiene que estar añadida con anterioridad.

Luego deberemos de poner el siguiente comando para generar el sitio jekyll

> jekyll new [nombre_repositorio]

(Los nombres del directorio y del repositorio deben de ser iguales para no tener problemas.)

Ahi si vemos los ficheros ya sea con un "ls" o directamente mirando el explorador del Visual Studio Code.

## Paso 4 Crear un post

Para ello deberemos de ir a la parte de exploracion del fichero donde esta nuestro sitio.
En el hay un fichero donde podremos cambiar la configuracion y editar nuestro sitio web que se llama "_config.yml".

Para crear los sitios deberemos de crear un markdown del post que queramos crear, este debe tener indicado lo siguiente:

---
`Layout: post`
`title: "Titulo del post"`
`"categories: Jekyll update"`
---
 y luego siempre guardarlo.


