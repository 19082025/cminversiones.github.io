# Starter web gratis (ES)

Este paquete es un *starter* estático listo para publicar **gratis** con tu dominio de **GoDaddy** usando:

- **GitHub Pages** (recomendado si no necesitas base de datos ni backend)
- **Netlify** (muy fácil, formularios incluidos)
- **Vercel** o **Cloudflare Pages** (también gratis)

Incluye:
- `index.html`, `about.html`, `contact.html`, `styles.css`
- Formulario de ejemplo que funciona en **Netlify** (atributo `data-netlify="true"`).

---

## Publicar en GitHub Pages (gratis)

1. Crea una cuenta en GitHub y verifica tu email.
2. Crea un repositorio llamado **`TUUSUARIO.github.io`** (reemplaza TUUSUARIO por tu usuario de GitHub).
3. Sube los archivos de este starter al repositorio (Upload files) y guarda cambios.
4. En **Settings → Pages**, confirma que la fuente (Branch) sea **`main`** con carpeta **`/`**. GitHub servirá tu web en `https://TUUSUARIO.github.io`.
5. (Opcional) En **Settings → Pages → Custom domain**, escribe tu dominio (por ejemplo, `www.tudominio.com`) y guarda. GitHub creará el archivo **CNAME** automáticamente.

### Conectar dominio de GoDaddy a GitHub Pages (www + root)
- En GoDaddy → **Mis productos → DNS** del dominio.
- Agrega un **CNAME**:
  - **Host:** `www`
  - **Apunta a:** `TUUSUARIO.github.io`
- Opcional: redirige el dominio raíz **tudominio.com** a **https://www.tudominio.com** con **Forwarding (301)** para evitar tocar registros A.
- Espera a que GitHub emita el certificado SSL y verás el candado activo.

> Nota: Si prefieres que el dominio raíz (sin www) apunte directo sin redirección, consulta la documentación de GitHub Pages para configurar registros **A** del raíz según los valores vigentes.

---

## Publicar en Netlify (gratis)
1. Entra a **app.netlify.com** con tu cuenta de GitHub (botón “New site from Git”).
2. Selecciona tu repositorio y haz Deploy (Netlify te da una URL temporal `*.netlify.app`).
3. En **Site settings → Domain management → Custom domains** añade tu dominio **www.tudominio.com**.
4. En GoDaddy añade un **CNAME**: `www` → `tu-sitio.netlify.app`.
5. (Opcional) Redirige **tudominio.com** → **https://www.tudominio.com** (Forwarding 301). Netlify gestiona SSL automáticamente.

---

## Publicar en Vercel o Cloudflare Pages
Ambas ofrecen planes gratis con dominio personalizado. El flujo es similar a Netlify: conectas tu repo, haces deploy y creas un **CNAME** `www` → subdominio que te asignen, y un **Forwarding** (301) desde el raíz si no manejas registros A.

---

## Editar el contenido
- Abre `index.html`, `about.html`, `contact.html` y cambia textos/links.
- Personaliza `styles.css` para tus colores/estilo.
- Sube cambios al repositorio y tu sitio se actualizará automáticamente.

---

## Mantener tu email de GoDaddy
No toques registros **MX**. Solo agrega CNAME de `www` y, si usas redirección, el **Forwarding** del dominio raíz. Así tu correo (por ejemplo `contacto@tudominio.com`) seguirá funcionando.
