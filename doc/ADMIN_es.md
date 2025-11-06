>[!WARNING]
> Hasta la versión 1.3.1, se aplica un **parche** para poder acceder a ciertas rutas. Proviene del repositorio de [GitHub de Saltcorn](https://github.com/saltcorn/saltcorn/issues/3660)
> El parche debe ejecutarse desde el botón "patcher" en el panel de control.
---

1️⃣  **Guía para el administrador y el usuario**

* [Wiki de Saltcorn](https://wiki.saltcorn.com/)
--- 

2️⃣ **Actualización**

Las actualizaciones de Saltcorn se gestionan a través de YunoHost: intentar actualizar desde la interfaz de Saltcorn no funcionará.

---

3️⃣ **Autenticación LDAP**

Si no se ha activado la autenticación LDAP durante la instalación, queda posible activarla en el **panel de configuración** o instalar el módulo LDAP en Saltcorn en (`Ajustes > Módulos`) y configurarlo con la siguiente información:

```
Server URL = ldap://127.0.0.1
Search Base = ou=users,dc=yunohost,dc=org
Search Filter = (|(mail={{username}})(uid={{username}}))
```
Los usuarios de YunoHost podrán iniciar sesión en Saltcorn, y el usuario administrador podrá modificar su rol.

⚠️ El usuario administrador **no puede iniciar sesión vía LDAP**.

---

4️⃣ **Copia de seguridad**

Las tablas se guardan en la base de datos.

* ⚠️ Al desinstalar Saltcorn, se perderán las tablas en la base de datos.
* Se guarda una copia de seguridad completa de las tablas cada semana en `/home/yunohost.app/saltcorn/backups` y es posible descargar las copias desde la interfaz de Saltcorn.
