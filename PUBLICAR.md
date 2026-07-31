# Cómo subirlo a GitHub

El repositorio ya está inicializado y con el primer commit hecho. Solo falta crearlo en GitHub y
hacer push.

## Opción A — con GitHub CLI (un comando)

Si tiene [GitHub CLI](https://cli.github.com/) instalado y con sesión iniciada (`gh auth login`),
desde esta carpeta:

```bash
gh repo create armando-mejia --public --source=. --push
```

Cambie `--public` por `--private` si prefiere que no sea visible.

## Opción B — sin GitHub CLI

1. Cree un repositorio vacío en <https://github.com/new>. Póngale el nombre `armando-mejia`
   y **no** marque «Add a README file».
2. Desde esta carpeta, ejecute:

```bash
git remote add origin https://github.com/USUARIO/armando-mejia.git
git push -u origin main
```

Reemplace `USUARIO` por su nombre de usuario de GitHub.

## Publicar el sitio en GitHub Pages

Con el repositorio ya subido:

**Settings → Pages → Source: «Deploy from a branch» → Branch: `main`, carpeta `/ (root)` → Save**

En dos o tres minutos el sitio queda en:

```
https://USUARIO.github.io/armando-mejia/
```

GitHub Pages en cuentas gratuitas requiere que el repositorio sea **público**. Si lo crea privado,
el sitio no se publicará, aunque el repositorio funcionará igual como respaldo.

## Dominio propio (opcional)

Si más adelante compra un dominio, por ejemplo `armandomejia.art`:

1. Cree un archivo llamado `CNAME` en la raíz del repositorio, con una sola línea:
   `armandomejia.art`
2. En el panel de su proveedor de dominio, apunte los registros `A` a las cuatro direcciones de
   GitHub Pages y el `CNAME` de `www` a `USUARIO.github.io`.
3. En **Settings → Pages → Custom domain**, escriba el dominio y active «Enforce HTTPS».

## Después de cada cambio

```bash
git add -A
git commit -m "Descripción del cambio"
git push
```

GitHub Pages vuelve a publicar solo, en un minuto aproximadamente.
