Antes de realizar la instalación del servidor apache debes buscar sus requisitos mínimos y comparalos con tu ordenador. ¿Puedes instalarlo?

1. Para realizar la instalación primero debemos actualizar los paquetes locales para se descarguen las nuevas versiones de los paquetes.

![Imagen 1](./images/1.PNG)
 
2. Después instalamos el paquete *apache2*.

![Imagen 2](./images/2.PNG)

3.El siguiente paso es modificar los ajustes del cortafuegos para que se garantice el acceso externo a los puertos web. Por defecto, tenemos un cortafuegos *UFW* configurado para restringir el acceso a nuestro servidor.
Durante la instalación se registran los perfiles que permitan habilitar o no su acceso a través del cortafuegos.
Listamos los perfiles con:

![Imagen 3](./images/3.PNG)

4.Como aún no hemos configurado el *SSL* para nuestro servidor solo permitiremos el tráfico a través del puerto 80

![Imagen 4](./images/4.PNG)

5.Podemos ver que realmente ha cambiado con este comando:

![Imagen 5](./images/5.PNG)

Si muestra que sigue inactivo sigue estos pasos, si no, salta hasta el décimo paso.

![Imagen 6](./images/6.PNG)

6.Para activarlo debemos asegurarnos de que en  el fichero *UFW* el valor de IPV6 sea *yes*.

![Imagen 7](./images/7.PNG)

![Imagen 8](./images/8.PNG)

7. Ahora debemos restablecer los valores predeterminados de las reglas *UFW*, para ello:

![Imagen 9](./images/9.PNG)

8. Si ahora habilitáramos el firewall de *UFW* denegaría todas las conexiones entrantes, para configurarlo de manera que permita las conexiones entrantes introduciremos el siguiente comando:

![Imagen 10](./images/10.PNG)

9.Por último solo debemos habilitar el UFW.

![Imagen 11](./images/11.PNG)

10. El servidor web debería estar ya activo y en ejecución, para verificar que está en correcto funcionamiento debemos introducir el siguiente comando y ver por pantalla el siguiente resultado:

![Imagen 12](./images/12.PNG)

11.OPCIONAL. Para saber con toda seguridad que nuestro servidor se ha instalado y funciona de manera correcta la mejor opción es solicitar una página web al servidor Apache. 
Si no sabemos la dirección IP de nuestro servidor introduciremos el siguiente comando y nos devolverá la IP.

![Imagen 13](./images/13.PNG)

Y accedemos desde el navegador de la siguiente manera: *http://ip_servidor*

![Imagen 14](./images/14.PNG)
