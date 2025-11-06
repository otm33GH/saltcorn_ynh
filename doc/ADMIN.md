> [!WARNING]
> Up to version 1.3.1, a **patch** is applied to access certain routes. It comes from the Saltcorn GitHub repository.
---
1️⃣ **Admin and User Documentation**

* [Wiki de Saltcorn](https://wiki.saltcorn.com/)
---

2️⃣ **Update**

Saltcorn updates are managed through YunoHost: trying to update from the Saltcorn interface will not work.

---
3️⃣ **LDAP Authentication**

If LDAP Authentication wasn't enabled during installation, it is possible to enable it in the **config panel**. Alternatively the LDAP module can be installed in Saltcorn under `Settings > Modules` and configure it with the following information:

```
Server URL = ldap://127.0.0.1
Search Base = ou=users,dc=yunohost,dc=org
Search Filter = (|(mail={{username}})(uid={{username}}))
```

* Yunohost users will be able to log in to Saltcorn, and the admin user will be able to modify their roles.

* ⚠️ The admin user **cannot log in via LDAP**.
---

4️⃣ **Backup**

Tables are saved in database. 
* ⚠️ If you remove Saltcorn, all your tables in database will be lost.
* A full backup of tables is performed each week and saved in `/home/yunohost.app/saltcorn/backups`. Backups can be downloaded.


