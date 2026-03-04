# ✏️ Cómo actualizar la web de Brainfulness

Hay 3 formas de actualizar la web, de más fácil a más técnica.

---

## OPCIÓN 1 — Pedirle a Befene (más fácil)

Escríbele a Befene por Telegram:
> "Cambia el texto de la sección Conferencias por este: ..."
> "Agrega este nuevo logo de institución: [imagen]"
> "Actualiza la foto de Lady por esta: [imagen]"

Befene hace el cambio, lo sube a GitHub y Netlify lo publica automáticamente en 30 segundos.

---

## OPCIÓN 2 — Editar el archivo HTML directamente (intermedio)

El archivo principal es uno solo: `index.html`

### Desde el Mac donde está el proyecto:
```bash
cd /Users/agentpc/.openclaw/workspace/brainfulness-web
open index.html  # Abre en el editor de texto
```

Haz el cambio, guarda, y luego:
```bash
git add .
git commit -m "Descripción del cambio"
git push
```

Netlify detecta el push y publica en 30 segundos. ✅

### Desde cualquier computador (GitHub web):
1. Ve a github.com → repositorio `brainfulness-web`
2. Clic en `index.html`
3. Clic en el lápiz ✏️ (Edit)
4. Haz el cambio
5. Clic en **"Commit changes"**

Netlify publica automáticamente. ✅

---

## OPCIÓN 3 — Instalar todo en un computador nuevo (técnico)

Si cambias de Mac o quieres que otra persona pueda editar:

```bash
# Instalar Git (si no lo tienen)
brew install git

# Clonar el repositorio
git clone https://github.com/TU_USUARIO/brainfulness-web.git

# Entrar a la carpeta
cd brainfulness-web

# Ver la web localmente
python3 -m http.server 8080
# Abrir: http://localhost:8080
```

---

## Cambios más comunes

### Cambiar un texto
Abre `index.html`, busca (Cmd+F) el texto que quieres cambiar, edita, guarda y sube.

### Cambiar una foto de perfil
1. Pon la nueva foto en `assets/lady.png` o `assets/juan.png`
2. Sube los cambios con `git push`

### Agregar un logo de institución
1. Pon el logo en `assets/logos/nuevo-logo.png`
2. En `index.html`, busca la sección `<!-- INSTITUCIONES -->`
3. Agrega: `<img src="assets/logos/nuevo-logo.png" alt="Nombre" class="logo-inst">`
4. Sube con `git push`

### Cambiar un video de YouTube
Busca en `index.html` el ID del video actual (ej: `jCT0S7TdTcs`) y reemplázalo por el ID del nuevo video (los últimos caracteres de la URL de YouTube).

### Actualizar métricas (reproducciones, países)
Busca en `index.html`:
- `+600K` → cambia por el nuevo número
- `108` (países) → cambia por el nuevo número

---

## Estructura de archivos

```
brainfulness-web/
├── index.html              ← EL archivo principal. Todo está aquí.
├── favicon-32.png          ← Ícono de la pestaña del navegador
├── apple-touch-icon.png    ← Ícono cuando se guarda en iPhone
├── assets/
│   ├── lady.png            ← Foto de Lady (con fondo transparente)
│   ├── juan.png            ← Foto de Juan (con fondo transparente)
│   ├── og-image.png        ← Imagen para compartir en redes sociales
│   ├── logos/              ← Logos de instituciones clientes
│   └── credenciales/
│       ├── lady/           ← Logos de formación académica de Lady
│       └── juan/           ← Logos de formación académica de Juan
├── GUIA-DEPLOY.md          ← Cómo subir la web al aire
└── COMO-ACTUALIZAR.md      ← Este archivo
```

---

## Reglas de oro

1. **Antes de hacer un cambio grande**, descarga una copia del `index.html` como respaldo
2. **Siempre haz `git push`** después de editar — si no, el cambio queda solo en tu Mac
3. **Para probar antes de publicar**: abre `index.html` directamente en Chrome (sin servidor)
4. **Si algo se rompe**: en GitHub puedes ver el historial y volver a una versión anterior

---

## ¿Necesitas más funcionalidades?

Cosas que requieren un desarrollador o Befene:
- Formularios de contacto con base de datos
- Integración con pasarela de pagos (para cursos)
- Sistema de usuarios y autenticación
- Blog con panel de administración

Para todo lo demás: edita `index.html` y listo.

---
*Documento creado por Befene — Marzo 2026*
