<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://www.sisenoragencia.com/">
    <img src="https://www.sisenoragencia.com/wp-content/uploads/2022/09/Grupo-4870.svg" alt="Logo" width="233" height="48">
  </a>

  <h3 align="center">Procedimiento para subir backups en los repositorios github.</h3>
  <p align="center">Readme creado por: Si Señor Agencia</p>
</div>

A continuación se enumeran los pasos a seguir para tener éxito en el envío de copias de seguridad a esta cuenta GitHub.

<ol>
    <li>Crear el repositorio desde la cuenta de la organización Si-Senor-Agencia-Backups
      <ul>
        <li>Ir a "Repositories"</li>
        <li>Click en "New repository"</li>
        <li>Generar nombre al nuevo repositorio en el input "Repository name". Preferiblemente usando el nombre del proyecto al cual piensa respaldar como backup y subirlo acá</li>
        <li>Aunque es opcional, es mejor que dé una descripción del proyecto en el apartado de "Description"</li>
        <li>Verificar que esté en "Private" el repositorio.</li>
        <li>Click en "Create repository"</li>
      </ul>
    </li>
    <li>Sigue el paso a paso y lo que esté entre comillas sencillas es el comando git a usar (No copiar las comillas sencillas):
      <ul>
        <li>'<b>git init</b>': Iniciamos git en la carpeta que contengan todos los archivos.</li>
        <li>'<b>git status</b>': Verifica el estado de los archivos de la carpeta. El color rojo que sale en la consola, terminal o similares sirve para entender que el repositorio local no está listo.</li>
        <li>'<b>git add .</b>': Enlista y prepara todos los archivos que se subiran al repositorio remoto</li>
        <li>'<b>git status</b>': Verifica nuevamente el estado para saber los archivos listos par enviar. El color verde indica que los archivos están listos</li>
        <li>'<b>git lfs install</b>': Instalamos Git LFS en el repositorio local. Previamente debe estar instalado el complemento git-lfs de manera global</li>
        <li>'<b>git lfs track "*.psd"</b>': Este comando selecciona los archivos que desee usar Git LFS (El comando se copia con las comillas dobles)</li>
        <li>'<b>git add .gitattributes</b>': Con el este comando se asegura el seguimiento de archivo elegido anteriormente en .gitattributes</li>
        <li>'<b>git add file.psd</b>': Agregamos el archivo o los archivos en cuestión para enviar al repositorios por medio de Git LFS</li>
        <li>'<b>git commit -m "first commit"</b>': Realizamos un commit, debe tener un mensaje claro y corto sobre el procedimiento. Si no tiene configurado globalmente git con una cuenta propia de github, debe ejecutar lo que indica la consola y preferible que no quede de forma global para que sepamos quién subió el backup en los commits</li>
        <li>'<b>git branch -M main</b>': Creamos la rama en el repositorio local.</li>
        <li>'<b>git remote add origin url-del-repositorio.git</b>': Conectamos el repositorio remoto al repositorio local y desde ahí subiremos todos los cambios. Reemplace la url del repositorio por el texto "url-del-repositorio.git"</li>
        <li>'<b>git push -u origin main</b>': Enviamos al repositorio remoto todos los archivos.</li>
        <li>En el momento que se intenta realizar el push del backup, se debe colocar las credenciales que se encuentran en el archivo de "Accesos 2023 | Si Señor"</li>
      </ul>
    </li>
</ol>
