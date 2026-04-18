Sistema de Gestión de Encomiendas

Proyecto desarrollado con Django + Docker + PostgreSQL, que simula un sistema de gestión de encomiendas con administración, control de estados y estructura modular por aplicaciones.

📌 Tecnologías utilizadas
Python 3.11
Django 6
PostgreSQL
Docker & Docker Compose
psycopg2-binary
python-decouple
🧱 Arquitectura del proyecto

El sistema está organizado en aplicaciones independientes (apps):

📦 envios → Gestión de encomiendas
👤 clientes → Gestión de clientes
🛣️ rutas → Gestión de rutas de envío
⚙️ Instalación y ejecución
1. Clonar repositorio
git clone https://github.com/KelvinRomC-gif/Encomienda.git
cd Encomienda
2. Configurar variables de entorno

Crear archivo .env:

SECRET_KEY=tu_clave
DEBUG=True

DB_ENGINE=django.db.backends.postgresql
DB_NAME=encomiendas_db
DB_USER=encomiendas_user
DB_PASSWORD=encomiendas_pass_2026
DB_HOST=db
DB_PORT=5432
3. Levantar el proyecto con Docker
docker compose up --build -d
4. Aplicar migraciones
docker compose exec web python manage.py makemigrations
docker compose exec web python manage.py migrate
5. Crear superusuario
docker compose exec web python manage.py createsuperuser
🌐 Acceso al sistema
Aplicación web:
http://localhost:8000
Panel de administración:
http://localhost:8000/admin