# NautaPy

__NautaPy__ Python API para el portal cautivo [Nauta](https://secure.etecsa.net:8443/) de Cuba + CLI.

## Requisitos

1. Instale la última versión estable de [Python3](https://www.python.org/downloads/)

## Instalación

Instalación:

```bash
pip3 install --upgrade git+https://github.com/Alex-diaz00/nauta-cli.git
```

## Modo de uso

### Agrega un usuario

```bash
nauta users add periquito@nauta.com.cu
```

Introducir la contraseña cuando se pida. Cambie `periquito@nauta.com.cu` por
su usuario Nauta.

### Iniciar sesión

Especificar el usuario

```bash
nauta up periquito
```

Se muestra el tiempo en el terminal, para cerrar la sesión se debe pulsar `Ctrl+C`.

* Opcionalmente puede especificar la duración máxima para la sesión, luego de la cual se desconecta automáticamente:

    ```bash
    nauta up --session-time 60 periquito
    ```

    El ejemplo anterior mantiene abierta la sesión durante un minuto.

Para iniciar la sesión con el usuario predeterminado sin necesidad de especificar el usuario utilice

```bash
nauta up
```

### Mantener la sesión activa siempre

Esta opción es útil si:

* Desea garantizar una conexión permanente a internet
* La conexión con el router se pierde ( afectación eléctrica, etc)
* Afectaciones internas del servicio de nauta hogar o políticas que definen un tiempo límite máximo por sesión por usuario

Agregar el parametro -k

```bash
nauta up -k
```

El comando iniciará la sesión. Si pierde la conexión con el router o la sesión se cierra, creará una nueva. Para detener su ejecución presione `Ctrl+C` dos veces seguidas.

### Ejecutar un comando con conexión

```bash
run-connected <cmd>
```
Ejecuta la tarea especificada con conexión, la conexión se cierra al finalizar la tarea.

### Consultar información del usuario

```bash
nauta info periquito
```

__Salida__:

```text
Usuario Nauta: periquito@nauta.com.cu
Tiempo restante: 02:14:24
```

### Determinar si hay conexión a internet

```bash
nauta is-online
```

__Salida__:

```text
Online: No
```

#### Determinar si hay una sesión abierta

```bash
nauta is-logged-in
```

__Salida__:

```text
Sesión activa: No
```

## Más Información

Lee la ayuda del módulo una vez instalado:

```bash
nauta --help
```

## Contribuir
__IMPORTANTE__: Notifícame por Twitter (enviar DM) sobre cualquier actividad en el proyecto (Issue o PR).

Todas las contribuciones son bienvenidas. Puedes ayudar trabajando en uno de los issues existentes.
Clona el repo, crea una rama para el issue que estés trabajando y cuando estés listo crea un Pull Request.

También puedes contribuir difundiendo esta herramienta entre tus amigos y en tus redes. Mientras
más grande sea la comunidad más sólido será el proyecto.

Si te gusta el proyecto dale una estrella para que otros lo encuentren más fácilmente.
