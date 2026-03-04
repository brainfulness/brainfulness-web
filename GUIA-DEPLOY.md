# 🚀 Guía completa: Llevar Brainfulness al aire
**Dominio:** brainfulness.life | **Hosting:** Netlify (gratis) | **Código:** GitHub

---

## PARTE 1 — Crear cuenta en GitHub (5 min)

GitHub es donde vive el código. Es tu respaldo permanente, independiente de Befene.

1. Ve a https://github.com/signup
2. Crea una cuenta con el email brainfulnesspodcast@gmail.com
3. Elige plan **Free**
4. Verifica el email

---

## PARTE 2 — Subir el código a GitHub (10 min)

1. En GitHub, clic en **"New repository"** (botón verde)
2. Nombre: `brainfulness-web`
3. Selecciona **Private** (solo ustedes lo ven)
4. Clic en **"Create repository"**
5. En tu Mac, abre Terminal y ejecuta:

```bash
cd /Users/agentpc/.openclaw/workspace/brainfulness-web
git init
git add .
git commit -m "Versión inicial Brainfulness web"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/brainfulness-web.git
git push -u origin main
```

*(Reemplaza TU_USUARIO con tu usuario de GitHub)*

✅ El código ya está en GitHub — aunque cambies de computador, el código está seguro.

---

## PARTE 3 — Crear cuenta en Netlify y conectar GitHub (10 min)

Netlify publica la web gratis y la actualiza automáticamente cada vez que cambias algo en GitHub.

1. Ve a https://netlify.com
2. Clic en **"Sign up"** → **"Sign up with GitHub"** (usa la cuenta que acabas de crear)
3. En el dashboard, clic en **"Add new site"** → **"Import an existing project"**
4. Selecciona **GitHub**
5. Busca y selecciona el repositorio `brainfulness-web`
6. Configuración del deploy:
   - **Branch to deploy:** `main`
   - **Base directory:** (dejar vacío)
   - **Build command:** (dejar vacío)
   - **Publish directory:** `.` (un punto)
7. Clic en **"Deploy brainfulness-web"**

En 30 segundos la web estará live en una URL tipo: `https://brainfulness-abc123.netlify.app`

---

## PARTE 4 — Conectar el dominio brainfulness.life (15 min)

### En Netlify:
1. Ve a tu sitio → **"Domain management"** → **"Add custom domain"**
2. Escribe: `brainfulness.life`
3. Clic en **"Verify"** → **"Add domain"**
4. Netlify te mostrará unos valores DNS. Necesitas 2 cosas:
   - **Netlify's load balancer IP** (algo como `75.2.60.5`)
   - O los **nameservers de Netlify**

### En GoDaddy:
1. Entra a https://godaddy.com → **Mis productos** → **brainfulness.life** → **DNS**
2. Busca el registro tipo **A** que apunta a `@`
3. Cambia el valor por la **IP de Netlify** que te dio en el paso anterior
4. Guarda los cambios

⏱️ Los cambios de DNS demoran entre **10 minutos y 48 horas** en propagarse. Normalmente menos de 1 hora.

### SSL (HTTPS) — automático:
Netlify activa el certificado SSL gratis automáticamente. Solo espera que el DNS propague y verás el candado verde.

---

## PARTE 5 — Verificar que todo funciona

1. Entra a https://brainfulness.life
2. Verifica el candado HTTPS en el navegador
3. Prueba todos los links del nav
4. Comparte el link en WhatsApp y verifica que sale la previsualización con imagen (og:image)

---

## PARTE 6 — Dominio alternativo (opcional)

**¿Vale la pena cambiar a bfn.com u otro?**

❌ No recomiendo cambiar. `brainfulness.life` es perfecto:
- Ya lo tienen pagado en GoDaddy
- Es memorable y on-brand
- `.life` refuerza el mensaje de bienestar
- Redirigir después tiene costo SEO

Si algún día quieren un dominio más corto, pueden comprar `bfn.co` (~$15/año) y redirigirlo a `brainfulness.life` sin perder nada.

---

## PARTE 7 — Cómo actualizar la web en el futuro

Ver archivo separado: **COMO-ACTUALIZAR.md**

---

## Resumen de cuentas necesarias

| Servicio | URL | Costo |
|----------|-----|-------|
| GitHub | github.com | Gratis |
| Netlify | netlify.com | Gratis (hasta 100GB/mes) |
| GoDaddy | godaddy.com | Ya tienen el dominio |

**Total costo mensual: $0**

---

## Contactos de soporte

- **Netlify docs:** https://docs.netlify.com
- **GitHub docs:** https://docs.github.com
- **Befene (Befene):** Telegram @Befene — para cualquier cambio de código

---
*Documento creado por Befene — Marzo 2026*
