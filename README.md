# Landing CardioElectroRM

Landing page del programa de formación en ECG del Dr. Rubelin Mosquea.

## ¿Qué hay acá?

Solo 2 archivos relevantes:

- **`index.html`** — toda la landing en un solo archivo (HTML + CSS + JS embebidos)
- **`bg-ecg.jpg`** — imagen de fondo (el ECG que se ve borroso atrás)

No hay build step, no hay dependencias, no hay framework. Es HTML plano.

## Cómo modificar el contenido

Abrí `index.html` en cualquier editor (VSCode, Sublime, hasta el Bloc de Notas sirve) y editás directo.

Las partes que vas a tocar más seguido están bien identificadas con comentarios:

```html
<!-- HEADER: Headline + Subheadline -->
<!-- VSL + CTA -->
```

### Cambiar el video de Vimeo

Buscá la línea con `player.vimeo.com/video/...` y cambiá el ID del video.

```html
src="https://player.vimeo.com/video/1189511401?..."
                                  ^^^^^^^^^^
                                  ID del video
```

⚠️ Asegurate que el video en Vimeo tenga la privacidad configurada para permitir embed. En Vimeo: **Settings → Privacy → "Where can this video be embedded?" → "Anywhere"**.

### Cambiar el formulario (Typeform)

Buscá `data-tf-popup="Bscuh1Aw"` y reemplazá `Bscuh1Aw` por el ID de tu propio Typeform.

### Cambiar texto del headline / subheadline / CTA

Solo edita el texto entre las etiquetas. Por ejemplo:

```html
<h1>Deja de derivar pacientes...</h1>   ← cambiá este texto
```

## Cómo publicar (deploy)

Cualquiera de estas plataformas funciona en 1 minuto y son **gratis**:

### Opción 1 — Vercel (recomendado)

1. Crear cuenta en [vercel.com](https://vercel.com)
2. "New Project" → importá este repo
3. Click "Deploy" — sin configurar nada
4. Te dan un dominio tipo `cardioelectrorm.vercel.app`

### Opción 2 — Netlify

1. Crear cuenta en [netlify.com](https://netlify.com)
2. "Add new site" → "Deploy with GitHub"
3. Elegir este repo
4. Deploy

### Opción 3 — GitHub Pages

1. En este repo → Settings → Pages
2. Source: `main` branch / root
3. Save → en 30 segundos tenés URL `snzzzzz.github.io/cardioelectrorm-landing`

## Conectar dominio propio

Cualquiera de las 3 plataformas te permite agregar `cardioelectrorm.com` como dominio custom. El paso a paso de cada una está en su documentación, pero básicamente:

1. En la plataforma, agregar el dominio
2. Te dan unos registros DNS (A o CNAME)
3. Los configurás en el panel de tu registrador (NameSilo, Namecheap, GoDaddy, etc.)
4. En 5-30 minutos propaga

## Stack técnico

- HTML5 + CSS inline + JavaScript inline
- Fuente: [Inter](https://fonts.google.com/specimen/Inter) cargada desde Google Fonts
- Video: iframe embebido de Vimeo
- Formulario: Typeform popup vía SDK oficial (`embed.typeform.com/next/embed.js`)

No usa React, Next, ni ningún framework. Funciona en cualquier hosting estático.

## Soporte

Cualquier duda técnica, contactar a quien te entregó esto.
