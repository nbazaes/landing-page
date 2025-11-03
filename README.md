# Landing Page

Pequeña landing para presentar un producto/servicio.

## Tecnologías: HTML, CSS, JS (opcional: Vite/React)

## Instalación:
1. git clone <repo>
2. cd landing-page
3. npm install (si aplica)

## Uso:
- Desarrollo: npm run dev
- Build: npm run build
- Servir dist localmente: npm run serve

## Deploy: Nginx
1. Generar build: npm run build
2. Copiar la carpeta dist al servidor, por ejemplo /var/www/landing
3. Crear un bloque de servidor en /etc/nginx/sites-available/landing, ejemplo:
    server {
         listen 80;
         server_name ejemplo.com;
         root /var/www/landing;
         index index.html;
         location / {
              try_files $uri $uri/ /index.html;
         }
    }
4. Activar y recargar nginx:
    sudo ln -s /etc/nginx/sites-available/landing /etc/nginx/sites-enabled/
    sudo nginx -t && sudo systemctl reload nginx

Licencia: MIT
