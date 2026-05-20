# Resend Email Server

Servidor Express para enviar correos usando la API de Resend. Listo para desplegar en Railway.

## Variables de entorno

Configura estas variables en Railway (Settings → Variables):

| Variable | Valor |
|---|---|
| `RESEND_API_KEY` | Tu API key de Resend |
| `FROM_EMAIL` | hola@telecola.site |

## Desplegar en Railway

1. Sube este proyecto a un repositorio de GitHub
2. En [railway.app](https://railway.app) → **New Project** → **Deploy from GitHub repo**
3. Selecciona el repositorio
4. Ve a **Variables** y agrega `RESEND_API_KEY` y `FROM_EMAIL`
5. Railway detecta automáticamente el `package.json` y ejecuta `npm start`
6. En **Settings → Networking** genera un dominio público

## Estructura

```
resend-server/
├── server.js          # Backend Express + Resend
├── public/
│   └── index.html     # Frontend con el botón de envío
├── package.json
├── .env.example
└── .gitignore
```

## Uso local

```bash
npm install
cp .env.example .env
npm start
# Abre http://localhost:3000
```
