> [!WARNING]
> Jusqu'à la version 1.3.1, un **patch** est appliqué pour pouvoir accéder à certaines routes. Il provient du [dépôt github de saltcorn](https://github.com/saltcorn/saltcorn/issues/3660).

---

1️⃣  **Documentation admin et utilisateur** 

* [Wiki de Saltcorn](https://wiki.saltcorn.com/)

--- 

2️⃣ **Mise à jour**  

 La mise à jour de Saltcorn est gérée depuis yunohost : essayer de mettre à jour depuis l'interface de Saltcorn ne fonctionnera pas.

--- 

3️⃣ **Authentification LDAP**

Si l'authentification LDAP n'a pas été activée à l'installation, il est possible de l'activer dans le **panneau de configuration**. Il est aussi possible d'installer le module LDAP dans Salcorn dans `Réglages > Modules` et de le paramétrer avec les informations suivantes:
```
Server URL = ldap://127.0.0.1
Search Base = ou=users,dc=yunohost,dc=org
Search Filter = (|(mail={{username}})(uid={{username}}))
```


* :white_check_mark: Les utilisateurs Yunohost pourront se connecter à Saltcorn et l'utilisateur administrateur pourra modifier leur rôle.  
* ⚠️ L'utilisateur administrateur **ne peut pas se connecter en LDAP**

---

4️⃣ **Sauvegarde**
Les tables sont enregistrées dans la base de données.

* ⚠️ Si Saltcorn est désinstallé, la base de données est perdue.
* Une copie de sauvegarde automatique de toutes les tables est réalisée chaque semaine dans `/home/yunohost.app/saltcorn/backups`. Les archives sont téléchargeables depuis l'interface de Saltcorn.
