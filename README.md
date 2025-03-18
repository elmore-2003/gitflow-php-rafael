"# gitflow-php-rafael"  

1. Creación del repositorio y configuración inicial

  # Hemos creado el repositorio con nuetro nombre 
  
    (gitflow-php-rafael)
    
  # Hemos clonado el repositorio en nuestro equipo local
  
    git clone https://github.com/elmore-2003/gitflow-php-rafael.git
  
  # Hemos iniciado Git Flow con el siguiente comando
  
    git flow init
  
  # Con el siguiente comando verificamos si la rama develop esta creada
  
    git branch -a 
  
    (si no esta creada utilizaremos el siguiente comando)
  
    git checkout -b develop
    git push origin develop
  
2. Creación de un archivo php

  # Creamos la nueva funcinalidad con el siguiente comando ¡:
  
    git flow feature start crear-mi-archivo
  
  # Creamos la carpeta alumnos y dentro un archivo llamado rafael.php con el siguiente codigo:
  
    <?php
    // Archivo: alumnos/tu_nombre.php
    echo "Hola, soy [Tu Nombre] y estoy aprendiendo Git Flow!";
    ?>
  
  # Subimos los cambios:
  
    git add alumnos/rafael.php
    git commit -m "Añadir php"
    git flow feature finish crear-mi-archivo
    git push origin develop

3. Modificación de un archivo existente

  # Creamos la nueva funcionalidad

    git flow feature start modificar-index

  # Creamos el archivo index.php con el siguiente contenido:

    <?php
    include "alumnos/tu_nombre.php";
    ?>

  # Ver cambios antes de confirmar con el siguiente comando:

    git diff

  # Subimos los cambios:

    git add index.php
    git commit -m "modificar index.php"
    git flow feature finish modificar-index
    git push origin develop

   
4. Resolución de conflictos

  # Modificamos el index en la misma línea que un compañero

  # Intentar hacer el merge en develop

    git checkout develop
    git merge feature/modificar-index

  # Resolver conflicto manualmente 

    buscamos las marcas <<<<<<<, ======= y >>>>>>> y lo edítamos correctamente.

  # Subimos los cambios:

    git add index.php
    git commit -m "Resolver conflicto en index.php"
    git push origin develop
  
6. Eliminación de un archivo
7. Publicación de la versión final
