# Compteur Jours Sans Accident

Application web statique pour MagicInfo, hébergée sur GitHub Pages.

## Fichiers

- `index.html` — écran principal (pour MagicInfo).
- `admin.html` — panneau d'administration (génère un nouveau `data.json`).
- `data.json` — données partagées (date du dernier accident, record).
- `foto.jpg` — image affichée à droite (à ajouter manuellement).

## Setup GitHub Pages (une seule fois)

1. Crear cuenta en https://github.com si no tienes.
2. Crear repo nuevo: `New repository` → nombre (ej. `securite-pantalla`) → **Public** → Create.
3. Subir los 4 archivos (drag & drop en la web del repo).
4. En el repo: `Settings` → `Pages` → Source: `Deploy from a branch` → Branch: `main` / `(root)` → Save.
5. Esperar 1-2 minutos. GitHub te dará la URL pública, algo como:
   `https://TU-USUARIO.github.io/securite-pantalla/`
6. Dar a MagicInfo la URL: `https://TU-USUARIO.github.io/securite-pantalla/index.html`
7. (Opcional) Configurar MagicInfo para recargar la página cada 5-10 minutos.

## Uso diario

### Ver el contador
Solo abrir la URL de `index.html`. Los días suben automáticamente cada día.

### Registrar un accidente / cambiar fecha / record
1. Abrir `https://TU-USUARIO.github.io/securite-pantalla/admin.html` en tu navegador.
2. Hacer los cambios.
3. Clicar **TÉLÉCHARGER data.json**.
4. Ir al repo de GitHub, abrir `data.json`, clic en el lápiz (editar) o arrastrar el archivo descargado encima para reemplazarlo.
5. Commit. En 1-2 minutos la pantalla muestra los nuevos datos.

## Notas

- El récord se actualiza solo en la pantalla mientras los días superen el récord guardado. Para fijarlo definitivamente, usar admin (registrar accidente o editar récord manualmente).
- `index.html` recarga `data.json` cada 60s con cache busting.
- Recarga completa programada cada noche a las 00:05.
