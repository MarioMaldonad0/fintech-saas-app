# Fintech SaaS App

Monorepo con 3 aplicaciones React y una API TypeScript, orquestado con Docker Compose y PostgreSQL.

## Estructura

```
fintech-saas-app/
├── users-front/     # React + Vite → http://localhost:5173
├── portal/          # React + Vite → http://localhost:5174
├── dashboard/       # React + Vite → http://localhost:5175
├── backend/         # TypeScript + Express → http://localhost:3000
├── docker-compose.yml
└── .env.example
```

## Inicio rápido

### Con Docker Compose (producción)
```bash
cp .env.example .env
# Editá .env con tus valores
docker compose up --build
```

### Desarrollo local

**Backend:**
```bash
cd backend
npm install
npm run dev
```

**React apps** (mismo proceso para portal y dashboard):
```bash
cd users-front
npm install
npm run dev
```

## Servicios

| Servicio     | URL local               | Descripción          |
|--------------|-------------------------|----------------------|
| users-front  | http://localhost:5173   | App de usuarios      |
| portal       | http://localhost:5174   | Portal principal     |
| dashboard    | http://localhost:5175   | Panel de control     |
| backend      | http://localhost:3000   | API REST             |
| postgres     | localhost:5432          | Base de datos        |

## Variables de entorno

Copiá `.env.example` a `.env` y completá los valores:

```bash
cp .env.example .env
```


# 1. Copiar variables de entorno
cp .env.example .env
# Editá .env con tus credenciales de DB

# 2. Levantar todos los servicios
docker-compose up --build

# 3. Verificar backend
curl http://localhost:3000/health
# → {"status":"ok","db":"connected"}

