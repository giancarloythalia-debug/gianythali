# Nuestros Gastos — App web (versión para GitHub Pages)

App de gastos de pareja en un solo archivo HTML, con sincronización en línea
automática vía Firebase Realtime Database.

## Qué hay en esta carpeta

- `index.html` — la app completa (abrir esto). Ya viene con tu config de Firebase
  **"nuestros-gatos"** precargada, así que se conecta sola.
- `firebase.json` — config de hosting (solo si usás Firebase Hosting; para GitHub
  Pages no hace falta).

## Cómo subir a GitHub (GitHub Pages)

1. Creá un repo nuevo en github.com (público o privado, da igual).
2. Subí **solo el contenido de esta carpeta** al repo (como mínimo `index.html`).
   - Opción fácil: en la web de GitHub → botón "Add file → Upload files" y arrastrá
     `index.html`. O usá GitHub Desktop / git.
3. En el repo: **Settings → Pages** → Source: **Deploy from a branch** → rama
   `main` (o `master`) → carpeta `/ (root)` → Save.
4. Esperá ~1 minuto. Tu app queda online en:
   `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/`

## Cómo sincroniza (entre tu PC y el celular)

- La app guarda todo en tu **Firebase Realtime Database** (proyecto `nuestros-gatos`).
- Lo que ingresás en un dispositivo aparece al instante en el otro.
- Todos abren la **misma URL** arriba y ven lo mismo.
- A cada dispositivo le va a pedir login con los perfiles que ya tenés (Giancarlo ML / Thali).

## Base de datos de Firebase — reglas

Asegurate de que las reglas de la Realtime Database permitan lectura/escritura:

```json
{ "rules": { ".read": true, ".write": true } }
```

(Eso habilita la sincronización sin autenticación personal por perfil.)

## Respaldos

En la app: **⚙️ Ajustes → 💾 Respaldo de datos → 📥 Descargar respaldo**.
Además, el botón **💾 Guardar** (arriba) escribe los cambios dentro del propio
`index.html` si querés conservar una copia local con todo embebido.
