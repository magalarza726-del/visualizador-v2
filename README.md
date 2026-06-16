# Visualizador IO — versión web estática

Esta carpeta está lista para publicarse como una página web estática en GitHub Pages.

## Cómo subirlo a GitHub Pages

1. Crea un repositorio nuevo en GitHub.
2. Sube estos archivos al repositorio:
   - `index.html`
   - `assets/`
   - `.nojekyll`
   - `README.md`
3. En GitHub, entra a **Settings → Pages**.
4. En **Build and deployment**, elige:
   - **Source:** Deploy from a branch
   - **Branch:** `main`
   - **Folder:** `/root`
5. Guarda los cambios.

GitHub publicará la página en una URL parecida a:

```text
https://TU_USUARIO.github.io/NOMBRE_DEL_REPOSITORIO/
```

## Uso local

También puedes abrir `index.html` directamente en el navegador.

## Nota

Esta versión no requiere Streamlit, Python ni servidor backend. La aplicación funciona del lado del navegador.
