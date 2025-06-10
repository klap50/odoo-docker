# 🐳 Clase Docker - Odoo 17 Community

Este proyecto te permite levantar una aplicación real usando Docker: **Odoo 17 Community + PostgreSQL**.  
Es ideal para practicar cómo funcionan los contenedores, servicios y redes en Docker Compose.

---

## ✅ Requisitos previos

Asegurate de tener instalado:

- [Docker Desktop](https://www.docker.com/products/docker-desktop/) (Windows, macOS)
  - En Windows, requiere WSL 2 (Docker lo instala automáticamente)
- `git` (opcional pero recomendado)
- Navegador web

---

## 📦 ¿Qué se instala?

Este entorno contiene:

| Servicio | Imagen Docker | Puerto | Descripción |
|---------|----------------|--------|-------------|
| Odoo    | `odoo:17`      | 8069   | Aplicación ERP web |
| PostgreSQL | `postgres:13` | 5432 | Base de datos usada por Odoo |

---

## 🚀 Pasos para levantar el entorno

### 1. Clonar el repositorio

Abrí tu terminal (PowerShell, CMD o Git Bash):

```bash
git clone https://github.com/tu-usuario/odoo17_class.git
cd odoo17_class

2. Levantar los contenedores
docker compose up -d

3. Acceder a Odoo
Una vez levantado, abrí tu navegador y entrá a:
http://localhost:8069
Vas a ver la pantalla para crear una nueva base de datos.


📁 Archivos importantes del proyecto
docker-compose.yml: define los servicios Odoo y PostgreSQL, sus redes y volúmenes.

.env: contiene las variables como usuario y contraseña de la base de datos.

odoo.conf: archivo de configuración de Odoo (contraseña admin, conexión a PostgreSQL, etc.).

🧹 Cómo apagar o reiniciar
Para apagar los servicios:

docker compose down


Para reiniciar:
docker compose restart


💡 Consejos útiles
Si aparece un error sobre permisos en odoo.conf, asegurate que el archivo tenga permisos de escritura o esté montado correctamente.

Podés ver los logs de cada contenedor con:
docker logs odoo-1
docker logs db-1