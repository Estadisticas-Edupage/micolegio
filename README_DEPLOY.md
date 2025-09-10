# Deploy a Vercel (GitHub + Vercel)

## Estructura sugerida
```
/mi-colegio/
  ├─ index.html                 # portal listo (versión fusionada)
  ├─ colvia3.html              # tu formulario externo (opcional; sólo para index_fetch.html)
  ├─ index_fetch.html          # alternativa que usa fetch() para cargar colvia3.html
  └─ vercel.json               # config opcional
```

## Paso 1: Subir a GitHub
```bash
git init
git add .
git commit -m "Deploy inicial"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/mi-colegio.git
git push -u origin main
```

## Paso 2: Importar repo en Vercel
1. Ve a https://vercel.com/new → Import Git Repository → elige tu repo.
2. Framework: "Other". Build Command: (vacío). Output: (vacío o ".").
3. Deploy.

## Paso 3: Probar
- Portal: https://TU-PROYECTO.vercel.app/
- Formulario público: https://TU-PROYECTO.vercel.app/#public
- Portal Padres: https://TU-PROYECTO.vercel.app/#padres

### Notas
- `index.html` es la versión fusionada (no necesita `colvia3.html`).
- `index_fetch.html` carga `colvia3.html` con fetch (si prefieres mantener tu formulario aparte). Ajusta la ruta interna si lo mueves de carpeta.
- Cambios futuros: `git add . && git commit -m "update" && git push` → Vercel despliega solo.
