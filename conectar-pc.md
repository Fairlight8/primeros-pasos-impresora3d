
# Conexión de la impresora al PC

## Explicación

Las impresoras 3D imprimen siguiendo una lista de **comandos** especificados en un fichero GCODE. Simplificando mucho, es una sucesión de órdenes como:

 - Calienta el extrusor hasta 200º
 - Mueve la boquilla a la posición X=10, Y=5, Z=3
 - Empuja 5mm de filamento

Estas ordenes **se pueden enviar de forma manual desde un ordenador**, no solamente desde un fichero GCODE. 

## Procedimiento

1. Instalar un programa de control. Por ejemplo, **Pronterface** se usa mucho y es multiplataforma.

2. Instalar los **drivers de tu impresora** (sea una AnyCubic, una Creality, una Artillery, ...) para tu sistema operativo (Windows, Linux o Mac). 

3. Conectar la impresora y el PC con el cable suminstrado por el fabricante. Suele ser un **cable serie de tipo B** (el típico de impresora).

4. Abrir Pronterface. Antes de abrir la conexión, debemos **localizar el puerto (COM1, COM2, ...) y el baudrate (2400-250000)** con el que realizar la conexión. Si tienes los drivers bien instalados, pulsando el botón **"Port"**, en la esquina izquierda superior, te detectará automáticamente ambos parámetros. Si ambos son correctos, al pulsar **"Connect"** aparecerán unos comandos en el panel derecho.

5. A partir de aquí, en la parte inferior del panel derecho podemos **escribir las órdenes** que queramos ejecutar. De momento no sabrás que poner. Con el tiempo te quedarás con los comandos más habituales. Puedes probar con M503, que muestra un resumen de los ajustes de la impresora 3D.