Codigo fuente de www.tosdr.org español. 

<!--Overview
========

We welcome other people to copy this project for other specific purposes (like a ToS;DR specific for API terms) or for country-specific (translation and national law issues). Just:

 1. open a public mailing list for people to contribute and start translating,
 2. fork the code from https://github.com/tosdr/tosdr-build and translate, or adapt, etc.
 3. change the name and the logo, and have a look at the license (AGPL for HTML/JS/CSS and CC BY SA for JSON) 

-->

The data specification is available [on the wiki][wiki].

[wiki]: https://github.com/tosdr/tosdr.org/wiki


Clonar el repositorio
=====================

Hay submodulos en el repositorio. Para tenerlos todos, clona el repositorio con la opcion de recursividad 'git clone --recursive'.

Build
=====
La mayor parte de los codigo fuente de las paginas web estan en 'src/' (Aun hay algun archivo fuera de aqui).

 build:

1. Asegurate de tener los submodulos en la carpeta 'dist/' y que esta al dia (i.e. ejecutando 'git submodule add https://github.com/tosdr/tosdr.org.git dist' y 'cd dist && git pull').

    Los codigos fuente son usados para generar el contenido del repositorio [tosdr.org](https://github.com/tosdr/tosdr.org), generado en 'dist/'. 

2. ejecuta `npm install` en la raiz de este repositorio para asegurarte de que tienes todos los paquetes necesarios.
3. Haz los cambios que desees a las fuentre de este repositorio.
4. Ejecuta 'grunt' en la raiz de este repositorio.
5. Comprueba que la salida en el directorio 'dist/' es como quieres.
6. Commit y push ambos repositorios.
7. Para publicar una nueva version de la pagina web, asumiendo que tienes 5 apps como remotas en 'dist/', ejecuta 'git push 5apps master'. Pero con cuidado: Estas actualizaciones son en directo sobre la pagina!!! Pregunta a [@hugoroy] o [@michielbdejong] si no tienes permisos.

[@hugoroy]: https://github.com/hugoroy
[@michielbdejong]: https://github.com/michielbdejong

<!-- This should have its own README
Import
======
To import new and/or updated threads from the Google Group:

* Open [import/bookmarklet.html](https://tosdr.org/import/bookmarklet.html) with Firefox, and follow instructions there; save result to `./import/newThreadSubjects.json` in your checked out local git repo
* create `./import/imapCredentials.js` from `./import/imapCredentials.js.sample`
* (from the repo root:) `git pull; npm install ; cd import ; mkdir rawPosts ; cd rawPosts ; node ../searcher.js`
* `cd .. ; node threadMatcher.js > ../index/threads.json`
* `cd .. ; node scripts/newPointsForNewThreads.js ; sh build.sh`
* `git add import/rawPosts ; git commit -am"import from Google Groups"; git push; git push 5apps master`

Curate
======
These scripts are what I (Michiel) currently use for curating points after import. The ideas is to integrate these into the web interface:

* `node scripts/curator.js` - will run a curating webinterface on http://localhost:21337/ that lets you change the (local) files on disk
* `node scripts/checkcases.js` - an interactive command-line tool that helps you assign cases to points that don't have one yet
* `node scripts/checkclasses.js` - outputs recommendations for adding/updating the class of services, based on their data points
-->


Desarollar otras aplicaciones
==========================

API: http://www.tosdr.org/api.html 

Mira tambien otras aplicaciones, como las extensiones del navegador: https://github.com/tosdr


Licencia
======

AGPL-3.0+ (GNU Affero General Public License, version 3 o superior)

Mira <https://tosdr.org/legal.html> Para mas detalles legales del proyecto.
