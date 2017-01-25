---
layout: post
title:  "Aprende a crear tu primer post"
date:   2017-01-05 05:30:24 -0300
categories: crear primer post
author: Hugo Páez Jiménez
author_tw: DerKows
author_fb: DerKow
author_gh: HPaez
---
Aprende como crear tu primer post en el blog de la comunidad, y también aprender como utilizar markdown.

<!--more-->

Hoy enseñaremos como crear un post en el blog de la comunidad y aportar a está.  
Primero realizaremos un fork al repositorio de [IV Devs](http://iv-devs.github.io/), accediendo en el siguiente link  <https://github.com/iv-devs/iv-devs.github.io>  
![Fotografía 1](http://image.prntscr.com/image/89faeea66ca54e32a44fa92ada6a2299.png)  
![Fotografía 2](http://image.prntscr.com/image/da7b59b68cd2438b8b5896a029796f1c.png)  
Luego de haber hecho el fork, clonamos el repositorio en nuestro computador o laptop e ingresamos a la carpeta creada  
![Fotografía 3](http://image.prntscr.com/image/d701ab8478134d909b3a1ba4d7246bee.png)  
Además, tendremos que crear una rama llamada post/nombre-del-post  
![Fotografía 4](http://image.prntscr.com/image/e9d835a22f2648b782f7e921ad1a10a2.png)  
Como siguiente paso creamos un archivo en la carpeta _posts, con la siguiente nomenclatura, YYYY-MM-DD-nombre-del-post.markdown, en el caso de este post, seria así “2017-01-05-como-crear-tu-primer-post.markdown”.  
![Fotografía 5](http://image.prntscr.com/image/b0395bbb601749b0b1b32381b97847be.png)  
Como quinto paso, por convención, el post debe llevar lo siguiente como cabecera  
```
---
layout: post
title:  "Titulo del post"
date:   YYYY-MM-DD HH:MM:SS -0300
categories: jekyll update
author: Author del post
author_tw: Twitter del Autor //Opcional
author_fb: Facebook del Autor //Opcional
author_gh: Github del autor //Opcional
---
Luego de esto escribimos algunas líneas como descripción del post y para finalizar la descripción escribimos lo siguiente  
<!--more-->
```
Algo como la siguiente imagen.    
![Fotografía 6](http://image.prntscr.com/image/fc16c889cf38455a9c7119927026e51c.png)  
Para poder ver los cambios y todo, es necesario tener instalado Ruby (no necesariamente rails) y ejecutar las siguientes instrucciones:  
```
gem install jekyll bundler
bundle install
bundle exec jekyll serve
```
Luego de ejecutar las instrucciones, podremos ingresar en el siguiente enlace <http://localhost:4000>  
Ya teniendo todo esto listo, ahora solo queda vez algunos tips:  
Como realizar un listado fácil, de estas dos formas:  
1. Prueba 1
2. Prueba 2
3. Prueba 3  

```
 1. Prueba 1
 2. Prueba 2
 3. Prueba 3
```
Otra forma es:  
* Prueba 1
* Prueba 2
* Prueba 3

```
 * Prueba 1
 * Prueba 2
 * Prueba 3
```

Como hacer cursiva:  
*Texto con cursiva*
```
*Texto con cursiva*
```

Segunda forma de hacer cursiva:  
_Texto con cursiva_
```
_Texto con cursiva_
```

Texto con negrita:  
**Texto en negrita**
```
**Texto en negrita**
```

Segunda forma de hacer negrita:  
__Texto en negrita__
```
__Texto en negrita__
```

Texto en negrita y cursiva:  
***Texto en negrita y cursiva***
```
***Texto en negrita y cursiva***
```
Segunda forma de hacer negrita y cursiva:  
___Texto en negrita y cursiva___
```
___Texto en negrita y cursiva___
```

Como realizar títulos para los post:  
Títulos (h1)  
# Título en h1
```
# Título en h1
```
Títulos (h2)  
## Título en h2
```
## Título en h2
```
Títulos (h3)  
### Título en h3
```
### Título en h3
```

Como ingresar un enlace a su post, existen varias formas   
Forma 1:  
[Texto a mostrar](http://ivdevs.com/ "texto al pasar el mouse")
```
[Texto a mostrar](http://ivdevs.com/ "texto al pasar el mouse")
```
Forma 2:  
[Texto a mostrar](http://ivdevs.com/)
```
[Texto a mostrar](http://ivdevs.com/)
```
Forma 3:  
<http://url>
```
<http://url>
```

Como hacer citas  
> Esto es una cita
>> Esto es una cita sobre una cita
> Esto es parte de la primera cita
```
> Esto es una cita
>> Esto es una cita sobre una cita
> Esto es parte de la primera cita
```
Dos formas de ingresar imágenes, la primera como mostrar una foto con titulo  
![Texto representativo](http://localhost:4000/img/logo.png "titulo")
```
![Texto representativo](http://localhost:4000/img/logo.png "titulo")
```

Segunda forma sin titulo  
![Texto representativo](http://localhost:4000/img/logo.png)
```
![Texto representativo](http://localhost:4000/img/logo.png)
```

Finalmente como subir estos cambios al blog  
Primero deberemos agregar nuestros cambios con:  
```
git add -A
```

Luego guardar estos cambios con:
```
git commit -m "Mensaje del commit. Preferentemente utilizar esta nomenclatura: CREATE 2017-01-05-como-crear-tu-primer-post"
```

También deberemos cambiarnos de rama con:
```
git checkout master
```

Mezclaremos la rama post con master con la siguiente instruccion:
```
git merge post/nombre-de-la-rama
Ej.
git merge post/how-to-create-a-post
```

Eliminamos la rama post
```
git branch -d post/nombre-de-la-rama
Ej.
git branch -d post/how-to-create-a-post
```

Subimos nuestros a cambios al repositorio con:
```
git push origin master
```

Al final deberia aparecer algo como la imagen siguiente:  
![Fotografía 7]()  