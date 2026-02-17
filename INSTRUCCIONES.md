# 📚 PASOS A SEGUIR (INSTRUCCIONES DETALLADAS)

## **PASO 1: Inicializar Git local** ✅ (LOCAL)
Abre PowerShell en esta carpeta y ejecuta:
```
git init
git add .
git commit -m "Primer commit"
```

## **PASO 2: Instalar Surge.sh** ✅ (LOCAL)
Abre PowerShell y ejecuta:
```
npm install -g surge
```
Después, ejecuta:
```
surge
```
- Te pedirá email y contraseña de Surge (crea una cuenta en surge.sh si no tienes)
- Elige un nombre de dominio (ej: miproyecto.surge.sh)
- Guarda el proyecto localmente (surge crea un archivo surge.json)
- **IMPORTANTE**: Copia el TOKEN que surge te proporciona (lo necesitarás para GitHub)

## **PASO 3: Crear repositorio en GitHub** ✅ (EN GITHUB)
1. Ve a github.com (inicia sesión)
2. Crea un nuevo repositorio (botón verde "New")
3. Nombre: `surgemika`
4. NO inicialices con README
5. Copia los comandos que te dan (serán similares a estos):

```
git remote add origin https://github.com/TU_USUARIO/surgemika.git
git branch -m main
git push -u origin main
```

## **PASO 4: Agregar Secrets en GitHub** ✅ (EN GITHUB)
1. Ve a tu repositorio en GitHub
2. Settings → Secrets and variables → Actions
3. Haz clic en "New repository secret"
4. Crea SURGE_DOMAIN:
   - Name: `SURGE_DOMAIN`
   - Value: `miproyecto.surge.sh` (el dominio que elegiste)
5. Crea SURGE_TOKEN:
   - Name: `SURGE_TOKEN`
   - Value: (el token que surge te dio globalmente)

📍 Para encontrar tu token globalmente:
   - En tu PC ve a: `C:\Users\TU_USUARIO\.netrc`
   - Abre con Notepad y copia el token que ves en surge

## **PASO 5: Pushear a GitHub** ✅ (LOCAL)
```
git remote add origin https://github.com/TU_USUARIO/surgemika.git
git branch -m main
git push -u origin main
```

## **PASO 6: Verificar que funciona** ✅
1. Ve a GitHub → tu repositorio → Actions
2. Verifica que el workflow se está ejecutando (circulito amarillo → verde)
3. Ve a tu dominio surge.sh (miproyecto.surge.sh) y deberías ver la página

---

## **¿Cómo editar la página después?**
1. Edita `index.html` localmente
2. Guarda los cambios
3. `git add .`
4. `git commit -m "Cambios realizados"`
5. `git push`
6. ¡Automáticamente se despliega a Surge! 🚀
