
# Modulo 0: Instalación y Configuracion de Git
Antes de empezar con el, es necesario que preparemos nuestro entorno e instalemos algunas librerias básicas. Al terminar este curso habrás:

- Instalado Git en tu ordenador.
	- Instalación en Linux
	- Instalación en MacOS
	- Instalación en Windows
- Configurado tu usuario local de git.
- Creado una cuenta en Github.

## Instalación de Git
Lo primero que haremos será instalar Git en tu ordenador.

### Instalación en Linux
Prácticamente, todas las distribuciones de Linux tienen instalado Git por definición. Lo primero que haremos será revisar si nuestro ordenador ya tiene Git. 

Para hacer esto es necesario que ejecutemos el siguiente comando en tu terminal:

```
git --version	// Este comando nos dirá la versión de git que tenemos instalada
```

De ejecutar este comando podemos esperar dos cosas. La primera es que tengamos git instalado y que obtengamos la siguiente respuesta de la terminal:

![git version](./imagenes/version.gif)

En caso de que tengamos ya instalado git hay que revisar que tenemos la última versión. En el caso del ejemplo anterior tenemos insatalada la version `2.14.2` que es la última versión estable disponible al momento de escribir este curso _(Revisa la última versión [aquí](https://git-scm.com/))_.

#### Git desactualizado o no instalado.
Si nuestra versión es menor a la ultima versión es menor o no tenemos instalado git será necesario ejecutar el siguiente comando en al terminal:

```
// Para sistemas operativos derivados de Debian:
sudo add-apt-repository ppa:git-core/ppa
sudo apt-get update
sudo apt-get install git

// Para sistemas operativos derivados de Fedora:
yum install git-core

```

¡Listo! :sparkles: Ejecutamos `git --version` para validar que ya tenemos git instalado. :tada:

### Instalación en MacOS
_Asegurate de tener instalado Xcode y la linea de comandos de Xcode_

MacOS tiene instalado por definición git. En el casó de que no tengas git instalado existen 3 formas en las que puedes instalarlo:

#### Instalación usando HomeBrew :beer:
[Homebrew](https://github.com/Homebrew/brew/) es un gestor de paquetes para MacOS que nos facilita el proceso de instalación de cualquier paquete así como la configuración necesaria para que funcione correctamente. Este gestor fue desarrolado por [Mike McQuaid](https://github.com/mikemcquaid).

Para instalar Homebrew ejecuta el comando:
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Instala Git:
```
brew install git
```

¡Listo! :beers: Ya tendremos instalada la última versión de git. Ejecuta el comando `git --version` en tu terminal para comprobar que esta instalado correctamente. :tada:

#### Instalación usando MacPorts :electric_plug:
Una alternativa a Homebrew es instalar git utilizando [MacPorts](https://www.macports.org/). MacPorts funciona de manera similar a Homebrew y busca facilitar los trabajos de instalación, actualización y compilado de la terminal.

para instalar MacPorts deberas bajar el instalador de la [página oficial](https://www.macports.org/install.php) e instalar el paquete. Después, ejecuta el comando:

```
sudo port install git-core +svn +doc +bash_completion +gitweb
```

¡Listo! Tendrás git instalado en tu ordenador. Ejecuta el comando `git --version` en tu terminal para comprobar que esta instalado correctamente. :tada:

#### Instalación usando Interfaz Gráfica
La última alternativa es instalar git usando la interfaz gráfica del instalador de Git que puedes descargar [aquí](http://sourceforge.net/projects/git-osx-installer/).

![Git Interfaz](./imagenes/git-int.png)

¡Listo! Tendrás git instalado en tu ordenador. Ejecuta el comando `git --version` en tu terminal para comprobar que esta instalado correctamente. :tada:

### Instalación en Windows
Hay multiples formas de instalar Git en Windows pero hay una unica solución que incluye todo lo necesario para poder seguir este curso. El proyecto Git for Windows` es la solución que usaremos. Descarga Git for Windows [aquí](https://git-for-windows.github.io/).

Una vez se haya instalado el programa en tu computadora también habrás instalado una shell con la que estaremos trabajando ya que incluye los mismos comandos que un sistema Unix tiene.

![Git Interfaz Windows](./imagenes/gw.png)

¡Listo! Tendrás git instalado en tu ordenador. Ejecuta el comando `git --version` en tu shell para comprobar que esta instalado correctamente. :tada:


## Configuración Local de Git
:sparkles: ¡Excelente! :sparkles: Ya tienes instalado git en tu ordenador. Ahora, solo hace falta configurar tu cuenta para que podamos empezar a utilizar git en tus proyectos.

Git tiene una herramienta llamada `git config` la cual te permite realizar las configuraciones de tu entorno de git. Existen un sin fin de configuraciones que puedes modificar en tu entorno, sin embargo, para este curso solo necesitamos configurar tu identidad.

Para hacer esto deberas ejecutar los siguientes comandos en tu terminal:
```
git config --global user.name "<TU NOMBRE>"
git config --global user.email <TU CORREO>
```

Ejemplo
```
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```

Por último comprobamos que se hayan guardado de forma correcta las configuraciones de tu entorno con el siguiente comando:

```
git config --list
```
Debes de obtener un resultado similar a:

```
$ git config --list
user.name=John Doe
user.email=johndoe@example.com
...
```
## Creación de Cuenta en GitHub

1. Primero vamos al sitio oficial de GitHub [https://github.com](https://github.com)
2. Damos click en `Sign Up`

![Step 1](./imagenes/step-1.png)

3. Llenamos el formulario con nuetros datos.

![Step 2](./imagenes/step-2.png)

4. Elegimos el plan gratuito.

![Step 3](./imagenes/step-3.png)

5. Llenamos el formulario final.
6. ¡Listo!
![Step 4](./imagenes/step-4.png)
