# quiz-m9
Ejercicio obligatorio para el modulo 9

La implementación del timeout de sesión utiliza una nueva variable llamada "req.session.time". Esta variable se crea y se inicializa con la estampilla de tiempo real desde el controlador de sesión, en el momento de crear una nueva sesión y se destruye desde la función que la cancela.

La supervisión del tiempo de inactividad se hace desde el middleware que implementa los "Helpers dinámicos", en app.js. Si al recibir una nueva petición se ha superado el tiempo máximo de 2 segundos, se destruirán las dos variables que controlan la sesión (req.session.time y req.session.user), en caso contrario, se guarda en req.session.time la estampilla de tiempo de la nueva petición.

La aplicación en Heroku está accesible en: https://quiz-2015-m9.herokuapp.com

El repositorio en Github está en: https://github.com/jpardo-interseven/quiz-m9

Saludos
