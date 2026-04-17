1)
git bisect usa búsqueda binaria sobre el historial de commits para encontrar el que introdujo un bug.
Necesitas:

    Un commit bad: donde el bug está presente (normalmente HEAD).
    Un commit good: anterior, donde sabes que el bug no existía.

Git va saltando a la mitad del rango, tú ejecutas una prueba (manual o automática) y le dices si ese commit es good o bad.
Tras varios pasos, te devuelve el primer commit donde apareció el bug.

2)
Por ejemplo si encontramos algún bug podemos marcarlo con el comando "git bisect bad" y hay que poner al final del comando el número de commit.

3)
Para que el proyecto sea eficaz hay que tener comportamiento deterministra, definición clara de éxito y fallo, el historial debe ser lineal, hay que conocer lo límites (bueno o malo) y velocidad de ejecución.
