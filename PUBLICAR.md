# Cómo publicar HERCULANEUM-299 en GitHub Pages

Guía completa. Si nunca hiciste esto, seguila paso a paso. Si ya conocés, andá directo a la parte 3.

## Parte 1: preparar los archivos en tu computadora

1. Descargá el ZIP que te pasé (o los cuatro archivos sueltos: `index.html`, `README.md`, `LICENSE`, `.gitignore`).

2. Creá una carpeta en tu computadora llamada `herculaneum-299` y poné los cuatro archivos adentro.

3. Verificá abriendo `index.html` en tu navegador que funcione local (haciendo doble click).

## Parte 2: crear el repositorio en GitHub

1. Entrá a https://github.com y hacé login (o creá cuenta si no tenés).

2. Arriba a la derecha, click en el **+** y elegí **New repository**.

3. Completá:
   - **Repository name:** `herculaneum-299` (o el nombre que quieras)
   - **Description:** "Ensayo especulativo interactivo sobre tejido temporal"
   - Elegí **Public**
   - **NO** marques "Add a README file" ni "Add .gitignore" ni "Choose a license" (ya los tenemos locales)

4. Click en **Create repository**.

## Parte 3: subir los archivos

### Opción A: por interfaz web (más fácil, recomendada si no usás git)

1. En la página del repo recién creado vas a ver instrucciones. Ignorá las de terminal.

2. Hacé click en **uploading an existing file** (link que aparece en la página vacía del repo).

3. Arrastrá los cuatro archivos (`index.html`, `README.md`, `LICENSE`, `.gitignore`) a la ventana.

4. Abajo, en "Commit changes", dejá el mensaje por defecto o escribí "Initial commit".

5. Click en **Commit changes**.

### Opción B: por terminal (si usás git)

```bash
cd herculaneum-299
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/herculaneum-299.git
git push -u origin main
```

(reemplazá `TU-USUARIO` por tu nombre de usuario real)

## Parte 4: activar GitHub Pages

1. En la página del repo, andá a **Settings** (arriba a la derecha).

2. En el menú izquierdo, click en **Pages**.

3. En "Source", elegí **Deploy from a branch**.

4. Debajo, en "Branch", elegí **main** (o **master** si tu repo usa ese nombre) y **/ (root)**.

5. Click en **Save**.

6. Esperá 1-2 minutos. Volvé a refrescar la página de Settings → Pages. Te va a mostrar un banner verde que dice: **"Your site is live at https://TU-USUARIO.github.io/herculaneum-299/"**

## Parte 5: actualizar el link en el README

1. Volvé a la página principal del repo.

2. Click en **README.md**.

3. Click en el ícono de lápiz (editar).

4. Reemplazá `TU-USUARIO` por tu nombre de usuario real en la línea del link.

5. Abajo, click en **Commit changes**.

## Parte 6: compartir

El link para compartir es: `https://TU-USUARIO.github.io/herculaneum-299/`

Funciona en desktop y mobile. Se carga rápido (es un solo HTML + una fuente externa).

Si querés un link más corto, podés usar servicios como bit.ly o is.gd, o comprar un dominio propio y apuntarlo al repo (se configura en Settings → Pages → Custom domain).

## Para actualizar contenido después

Cada vez que quieras cambiar algo, editás el archivo en GitHub (interfaz web) o lo pusheás desde tu terminal. GitHub Pages detecta el cambio y re-despliega automáticamente en 1-2 minutos.

## Troubleshooting

**"La página da 404"**
Esperá 5 minutos. A veces GitHub Pages tarda en la primera activación. Si después de 10 minutos sigue en 404, revisá que el branch y la carpeta estén bien configurados en Settings → Pages.

**"Se ve raro en celular"**
El HTML ya tiene viewport configurado. Si se ve raro, puede ser cache del navegador. Probá en una ventana privada o borrá el cache.

**"Las fuentes no cargan"**
El archivo carga Google Fonts por CDN. Si tu usuario está detrás de un firewall corporativo que bloquea fonts.googleapis.com, la tipografía cae a la del sistema. Funciona igual, solo se ve menos vintage.
