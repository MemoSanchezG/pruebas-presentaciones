# Simuladores de Señales de Transmisión

Simuladores interactivos del curso Señales de Transmisión (LSTI, FCFM-UANL), publicados con
GitHub Pages:

**https://memosanchezg.github.io/pruebas-presentaciones/**

- Cada simulador es una sola página HTML, sin bibliotecas externas: funciona en el celular y en
  la computadora, y sigue funcionando sin internet una vez abierto.
- El índice los ordena por fase y semana y tiene un buscador.
- En el pie de cada simulador, "Abrir en el celular (QR)" muestra su código QR, para proyectarlo
  en clase y que los estudiantes lo abran en su teléfono. El índice también trae el QR del sitio.

## Cómo se actualiza

Este repositorio es un sub-proyecto del repositorio privado del curso, donde vive como submódulo
en `sitio-simuladores/`. La fuente de los simuladores está en `presentaciones/simuladores/` de ese
repositorio, con las notas para el profesor y las respuestas en un comentario al inicio de cada
archivo. **No edites `docs/` a mano**: se genera con

```bash
python presentaciones/simuladores/publicar.py
```

que revisa los simuladores, les quita los comentarios (las notas y las respuestas no se publican),
agrega el QR y genera el índice, la página 404 y las redirecciones de direcciones viejas. Después:

```bash
cd sitio-simuladores
git add -A
git commit -m "Actualiza los simuladores"
git push
```

GitHub Pages (rama `main`, carpeta `/docs`) publica los cambios en uno o dos minutos.
