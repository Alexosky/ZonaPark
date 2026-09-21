# ZonaPark — Landing Page

Landing page del proyecto formativo **ZonaPark** (sistema de gestión de parqueaderos).
Programa de Análisis y Desarrollo de Software — SENA, Centro de Manufactura Avanzada, ficha 3229207.

## Contenido

| Archivo | Qué es |
|---|---|
| `index.html` | La página completa (HTML, CSS y JavaScript en un solo archivo, sin dependencias) |
| `assets/diagramas/` | Los 25 diagramas: procesos BPMN, actividades y secuencias |
| `assets/diagramas-procesos.pdf` | Documento original de los diagramas de procesos |
| `.nojekyll` | Evita que GitHub Pages ignore archivos; déjalo tal cual |

## Secciones de la página

1. Encabezado (título + logo)
2. Propuesta de valor — ¿Qué hacemos?
3. Beneficios principales
4. Diagramas — procesos, actividades y secuencias, filtrables por épica
5. Prueba social — cifras del proyecto
6. Llamado a la acción
7. Formulario de conversión
8. Preguntas frecuentes
9. Footer

## Publicar en GitHub Pages

1. Crear un repositorio nuevo (por ejemplo `zonapark`) y subir **el contenido de esta carpeta** a la raíz de la rama `main`.
2. En el repositorio: **Settings → Pages**.
3. En *Source* elegir **Deploy from a branch**, rama `main`, carpeta `/ (root)`. Guardar.
4. A los pocos minutos la página queda en `https://<usuario>.github.io/<repositorio>/`.

Comandos:

```bash
git init
git add .
git commit -m "Landing page ZonaPark"
git branch -M main
git remote add origin https://github.com/<usuario>/<repositorio>.git
git push -u origin main
```

## Conectar el formulario

El formulario **valida en el navegador y muestra la confirmación, pero todavía no envía los datos a ningún lado**, porque GitHub Pages solo sirve archivos estáticos y no tiene backend.

Para que envíe de verdad:

1. Crear un formulario gratuito en [formspree.io](https://formspree.io) (o similar) y copiar la URL que entregan.
2. Abrir `index.html`, buscar la línea:

   ```js
   var ENDPOINT = "";
   ```

3. Pegar la URL entre las comillas:

   ```js
   var ENDPOINT = "https://formspree.io/f/xxxxxxx";
   ```

Listo. El resto del código ya hace el envío y maneja el error si falla.

## Equipo

- Oscar Jairo Álvarez López
- Esteban Forero Deossa
- Mateo Vargas Martínez
- Adrián Alejandro Velázquez Petro

Instructor: Deimer Miranda Montoya
