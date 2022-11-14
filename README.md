# NginxPHP



    Realiza la configuración básica de nginx que ejecute scripts PHP creando una receta ansible. Utilizando como base la receta ansible que utilizaste para el taller 4, modifícala para añadir las siguientes funcionalidades:
        Instalación de los servicios (cada servicio se instalará y configurará en un rol diferenciado).
        Además de copiar un index.html en el DocumentRoot, copiará también un fichero info.php que muestre la información de la configuración de PHP.
        Como hace la receta original, creará virtualhost que tengas definido en una lista. Estos virtual host estarán configurados para ejecutar PHP.
        La receta debe poder desactivar los virtualhost que tengas definido en otra lista.

    Configura sobre una máquina virtual, usando la receta de ansible, un servidor nginx + PHP con dos virtualhost:
        www.pagina1.org, cuyo DocumetRoot estará en /srv/www/pagina1.
        www.pagina2.org, cuyo DocumetRoot estará en /srv/www/pagina2.

    Una vez que la receta haya configurado el servidor web con los dos Virtualhost, configura manualmente las siguientes características:
    Cuando se acceda a www.pagina1.org se realizará una redirección a a la página www.pagina1.org/principal. En el directorio principal no se permite ver la lista de los ficheros, no se permite que se siga los enlaces simbólicos.
    En la página www.pagina1.org/principal se debe mostrar una página web estática (utiliza alguna plantilla para que tenga hoja de estilo o la página estática que has generado en IAW).
    Si accedes a la página www.pagina1.org/principal/documentos se visualizarán los documentos que hay en /srv/doc. Por lo tanto se permitirá el listado de fichero y el seguimiento de enlaces simbólicos.
    Limita el acceso a la URL www.pagina1.org/secreto con autentificación básica.
