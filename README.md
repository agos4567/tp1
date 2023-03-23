### ¿Por qué es conveniente incluirlo?


Por que no todos los archivos y carpetas son necesarios de gestionar a partir del sistema de control de versiones. Hay código que no necesitas enviar a Git, ya sea porque sea privado para un desarrollador en concreto y no lo necesiten (o lo deban) conocer el resto de las personas. Pueden ser también archivos binarios con datos que no necesitas mantener en el control de versiones, como diagramas, instaladores de software, etc.


### ¿Cuándo se debe hacer?
 
se debe hacer al inicio del repositorio para tenerlo disponible en caso de necesitarlo.











### ¿Cómo configuraría el archivo .gitignore?


Para crear un archivo .gitignore local, crea un archivo de texto y asígnale el nombre ".gitignore" (recuerda incluir el . al principio). Luego, edita este archivo según sea necesario. Cada nueva línea debe incluir un archivo o carpeta adicional que quieras que Git lo ignore.

  Las entradas de este archivo también pueden seguir un patrón coincidente:

"*" se utiliza como una coincidencia comodín.
"/" se usa para ignorar las rutas relativas al archivo .gitignore.
"#" es usado para agregar comentarios
Este es un ejemplo de cómo puede lucir el archivo .gitignore :

- Ignora archivos del sistema Mac 
.DS_store

- Ignora la carpeta node_modules
node_modules

- Ignora todos los archivos de texto
*.txt

- Ignora los archivos relacionados a API keys
.env

- Ignora archivos de configuración SASS
.sass-cache
Para agregar o cambiar tu .gitignore global, ejecuta el siguiente comando en la terminal:

git config --global core.excludesfile ~/.gitignore_global
Esto creará el archivo ~/.gitignore_global. Ahora puedes editar ese archivo de la misma manera que un archivo .gitignore local. Todos tus repositorios Git ignorarán los archivos y carpetas listadas en el .gitignore global.
