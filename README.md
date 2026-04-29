# Stage Crono Puchuncaví — Gravitas Solutions

Sistema de cronometraje GPS · DH La Canela · 1 stage.

## Estructura
```
stage-crono-puchuncavi/
├── index.html          ← Home / sesión del piloto
├── crono.html          ← Cronómetro (carga seg01.js)
├── resultados.html     ← Leaderboard
├── assets/
│   ├── session.js      ← Sesión persistente + config Supabase + EVENTO='puchuncavi'
│   └── seg01.js        ← Stage único · DH La Canela (2.52 km, -504m)
├── icons/
├── manifest.json       ← PWA
└── sw.js               ← Service worker
```

## Uso
- `index.html` → ingresa nombre → arranca el stage
- `crono.html` → cronómetro DH (auto-carga seg01.js)
- `resultados.html` → Leaderboard del stage

## Datos del stage
- **Distancia**: 2.52 km
- **Desnivel**: 504 m (descenso puro)
- **Modalidad**: DH
- **Waypoints**: Inicio + 3 splits + Fin
- **Radio detección**: 45 m

## Backend
- Supabase compartido con Las Varas (proyecto `stage-crono-las-varas`)
- Tabla: `resultados` · columna `evento='puchuncavi'`
- Vistas: `mejores_tiempos`, `campeonato` (filtran por evento)

## GitHub Pages
Activar en Settings → Pages → Branch: main → / (root)
