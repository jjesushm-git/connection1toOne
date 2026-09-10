# connection1toOne v1.0.0

PWA para Android/Chrome orientada a chat local y envío de archivos entre dispositivos conectados a la misma red Wi‑Fi/hotspot.

## Publicar en GitHub Pages
1. Crea un repositorio nuevo.
2. Sube el contenido de esta carpeta a la raíz del repositorio.
3. Ve a Settings > Pages.
4. En Build and deployment selecciona Deploy from a branch.
5. Selecciona main y / (root), luego Save.
6. Abre la URL HTTPS que genere GitHub Pages.
7. En Android/Chrome usa "Instalar app" o "Agregar a pantalla principal".

## Cómo enlazar sin servidor
Esta versión usa WebRTC DataChannel y emparejamiento manual, para no necesitar Supabase ni un servidor de señalización.

- En el celular que comparte Wi‑Fi: Chat > Este celular comparte Wi‑Fi > elige Dip01, Dip02 o Dip03 > copia la invitación.
- En el otro dispositivo: abre la misma web > Chat > Soy dispositivo conectado > pega la invitación > genera respuesta.
- Devuelve esa respuesta al celular principal y pulsa Finalizar enlace.

Los mensajes y archivos se transfieren directamente entre navegadores. La bitácora se guarda localmente en IndexedDB.

## Límites
- Archivo máximo: 50 MB.
- Bitácora: máximo 20 chats.
- Protección: máximo 5 chats.
- Chats no protegidos: se eliminan al superar 24 horas desde su última actividad.
- GitHub Pages por sí solo no puede descubrir automáticamente otros dispositivos en el hotspot. Para conexión automática se necesitaría un servidor de señalización o una app Android nativa que ejecute un servidor local.
