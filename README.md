Pes Kit Archive

Archivo web de kits (equipaciones) de fútbol organizado por país y liga. Cubre las 211 federaciones afiliadas a la FIFA.

Cualquiera puede ver el archivo. Solo el administrador (con login) puede añadir y eliminar ligas y kits.

Cómo se usa
Elige un país (puedes filtrar por confederación o buscar por nombre).
Dentro del país, + Añadir liga: nombre, categoría, nivel, número de equipos, temporada y logo.
Dentro de la liga, + Añadir kit: equipo, temporada, tipo (local, visitante, tercera, portero, especial o retro), notas e imágenes.
Haz clic en cualquier imagen para verla en grande.

Las imágenes se comprimen automáticamente en el navegador (WebP, máximo 900 px) antes de subirse, para ahorrar espacio.

Tecnología
Una sola página index.html (HTML, CSS y JavaScript, sin dependencias de compilación).
Supabase como base de datos, almacenamiento de imágenes y login.
GitHub Pages para el hosting.
Instalación
Supabase: crea un proyecto gratuito. En SQL Editor ejecuta el contenido de schema.sql.
Usuario administrador: en Authentication → Users → Add user crea tu email y contraseña, y marca Auto Confirm User. Después desactiva Allow new users to sign up para que nadie más pueda registrarse.
Claves: en Project Settings → API copia la Project URL y la anon public key, y pégalas al principio del script de index.html:
js
   const SUPABASE_URL="https://TU-PROYECTO.supabase.co";
   const SUPABASE_KEY="TU-ANON-PUBLIC-KEY";

La clave anon es pública por diseño; la seguridad la dan las políticas de acceso de schema.sql. 4. GitHub Pages: en Settings → Pages, elige Deploy from a branch, rama main, carpeta / (root).

Estructura
Archivo	Para qué sirve
index.html	La web completa. Es lo único que se publica en GitHub Pages.
schema.sql	Se ejecuta una vez en Supabase para crear tablas, bucket de imágenes y permisos.
README.md	Este archivo.
Permisos
Lectura: pública, sin login.
Escritura (crear y borrar ligas, kits e imágenes): solo usuarios autenticados.
Aviso

Proyecto de aficionados sin ánimo de lucro. Los escudos y diseños de las equipaciones pertenecen a sus respectivos clubes, federaciones y fabricantes.
