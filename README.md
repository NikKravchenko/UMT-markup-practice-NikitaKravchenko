# Flora — Flower Shop (monorepo)

Responsive landing page for a flower shop with dynamic content, forms, modals, and a full-stack catalog backed by PostgreSQL.

Design: [Flora on Figma](https://www.figma.com/design/2Tj16H7IO7dq1ViTvIh57V/Flora?t=7olHeLo3vrfKuoc2-0)

## Live Demo

| Resource | URL |
|----------|-----|
| Frontend (GitHub Pages) | https://nikkravchenko.github.io/UMT-markup-practice-NikitaKravchenko/ |
| Backend API (Render) | https://umt-markup-practice-nikita-kravchenko.onrender.com/api |
| Swagger UI | https://umt-markup-practice-nikita-kravchenko.onrender.com/api-docs |

## Project Structure

```
backend/          # Express API (Render root directory)
frontend/         # Vite landing page (HTML, CSS, JS)
docs/             # production build for GitHub Pages (generated)
```

## Local Development

### Frontend

```bash
cd frontend
npm install
npm run dev
```

Open http://localhost:4000/UMT-markup-practice-NikitaKravchenko/

For the real API locally, create `frontend/.env`:

```env
VITE_API_MODE=server
VITE_API_BASE_URL=http://localhost:3000/api
VITE_BOUQUETS_API_URL=http://localhost:3000/api
```

Or from repo root:

```bash
npm run dev
```

### Backend

```bash
cd backend
npm install
cp .env.example .env
# set DATABASE_URL in .env
npm run seed
npm run dev
```

API: http://localhost:3000/api — Swagger: http://localhost:3000/api-docs

### Production Build

```bash
cd frontend
npm run build
```

Build output goes to `/docs` in the repo root (GitHub Pages).

Production uses `frontend/.env.production`: all sections load data from the Render API.

## Author

Nikita Kravchenko
