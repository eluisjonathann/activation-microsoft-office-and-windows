> **Copia de respaldo / alternativa:** [[Manual de activación segura y permanente de Windows (Copia alternativa)]]

Bienvenido a este manual técnico diseñado para usuarios que buscan activar su sistema operativo Windows de forma **oficial, permanente, ligera y 100% segura**, sin recurrir a cracks dudosos, activadores temporales o ejecutables maliciosos.

A diferencia de los métodos tradicionales obsoletos (como KMSPico, KMSAuto o herramientas empaquetadas en ejecutables opacos), esta guía utiliza **MAS (Microsoft Activation Scripts)**, el proyecto de código abierto más auditado, documentado y respetado a nivel mundial.

El objetivo es obtener una **Licencia Digital Permanente (HWID)** registrada directamente en los servidores de Microsoft y ligada a la placa base del equipo, garantizando un sistema completamente limpio, genuino y libre de servicios residentes.

| Opciones | ¿Por qué? |
| :--- | :--- |
| **Windows 10 / Windows 11** | Compatible con ediciones Home, Pro, Enterprise, Education y Workstations |
| **Licencia Digital (HWID)** | Método oficial permanente registrado en los servidores de activación de Microsoft |
| **MAS (Microsoft Activation Scripts)** | Código abierto, auditable, sin malware y sin requerir desactivar antivirus |
| **Cero Residuos en el Sistema** | No instala servicios en segundo plano ni modifica librerías del sistema operativo |

##### ⚠️ NOTA IMPORTANTE SOBRE SEGURIDAD

A diferencia de los activadores de terceros o de dudosa procedencia:
- ✅ Código 100% abierto y auditable en GitHub
- ✅ Registrado en los servidores legítimos de Microsoft
- ✅ No instala ningún archivo ejecutable permanente ni servicios en segundo plano
- ✅ No requiere desactivar Windows Defender ni ninguna suite de seguridad
- ✅ Si formateas o reinstalas Windows desde cero, se reactiva automáticamente por internet
- ✅ Desarrollado y verificado por la comunidad técnica internacional (*massgravel*)

---

## 🚀 MÉTODO 1: ACTIVACIÓN DIRECTA POR POWERSHELL (RECOMENDADO)

Este es el método oficial más rápido, limpio y recomendado: no requiere descargar archivos ZIP, descomprimir carpetas ni dejar archivos residuales en el almacenamiento.

### Paso 1.1: Abrir PowerShell como Administrador

1. Presiona la combinación de teclas:
```text
Win + X
```
2. En el menú emergente, selecciona:
   * **Terminal (Administrador)** o **Windows PowerShell (Administrador)**
3. Si aparece el aviso del Control de Cuentas de Usuario (UAC), haz clic en **"Sí"**.

*(Alternativa rápida: presiona `Win + R`, escribe `powershell` y presiona `Ctrl + Shift + Enter`).*

---

### Paso 1.2: Invocación Oficial del Script

Copia y pega cualquiera de las dos líneas oficiales en la ventana de PowerShell y presiona `Enter`:

**Comando principal:**
```powershell
irm https://get.masgrave.l | iex
```

**Comando alternativo / espejo oficial:**
```powershell
irm https://massgrave.dev/get | iex
```

> **¿Qué hace este comando?**  
> `irm` (*Invoke-RestMethod*) descarga en memoria el script oficial directamente desde el repositorio verificado y `iex` (*Invoke-Expression*) lo ejecuta en tiempo real sin guardar ningún archivo basura en disco.

---

### Paso 1.3: Navegar el Menú Principal

Al ejecutarse el comando, se abrirá la consola interactiva de MAS:

```text
Administrador: Microsoft Activation Scripts

------------------------------------------------------------------
    Activation Methods:
    [1] HWID           - Windows          ← ELIGE ESTA
    [2] Ohook          - Office
    [3] KMS38          - Windows
    [4] Online KMS     - Windows / Office
------------------------------------------------------------------
    [5] Check Activation Status
    [6] Change Windows Edition
------------------------------------------------------------------
    [0] Exit
------------------------------------------------------------------

Choose a menu option using your keyboard [1,2,3,4,5,6,0] :
```

**Escribe:** `1`  
**Presiona:** `Enter`

> **Nota para ediciones especiales (LTSC / Server):**  
> Si estás utilizando **Windows 10/11 Enterprise LTSC** o **Windows Server**, selecciona la opción **`[3] KMS38`**, la cual activa el sistema hasta el año 2038 de forma permanente sin requerir conexión continua a servidores KMS.

---

### Paso 1.4: Proceso de Generación y Registro de Licencia

Durante la ejecución verás en pantalla el procedimiento automatizado:

```text
Checking OS Info                     [Windows 11 Pro | 10.0.xxxxx | x64]
Initiating Diagnostic Tests...
Checking Registry Key                [Successful]
Installing Generic Product Key       [Professional] [VK7JG-NPHTM-C97JM-9MPGT-3V66T] [Successful]

Creating genuine ticket...           [Successful]
Applying genuine ticket...           [Successful]
Activating Windows...                [Successful]

Windows is permanently activated with a digital license.   ← ¡ESTO ES LO IMPORTANTE!
Help: https://massgrave.dev/troubleshoot

Press any key to Go back...
```

**Presiona cualquier tecla** para regresar al menú principal y luego presiona `0` para salir de MAS.

---

## 📦 MÉTODO 2: DESCARGA LOCAL / OFFLINE (ALTERNATIVA)

Si prefieres tener el paquete guardado localmente o ejecutarlo en un ordenador sin conexión inmediata:

### Método A: Descarga Directa del Paquete

1. Ingresa al enlace oficial de descarga del repositorio:
   [https://github.com/massgravel/Microsoft-Activation-Scripts/archive/refs/heads/master.zip](https://github.com/massgravel/Microsoft-Activation-Scripts/archive/refs/heads/master.zip)

```text
https://github.com/massgravel/Microsoft-Activation-Scripts/archive/refs/heads/master.zip
```

2. Guarda el archivo `Microsoft-Activation-Scripts-master.zip` en tu equipo.
3. Haz clic derecho sobre el archivo ZIP y selecciona **"Extraer todo..."**.
4. Ingresa a la carpeta extraída: `Microsoft-Activation-Scripts-master\MAS\All-In-One-Version\`.
5. Ubica el archivo: **`MAS_AIO.cmd`**.
6. Haz clic derecho sobre **`MAS_AIO.cmd`** y selecciona **"Ejecutar como administrador"**.
7. Selecciona la opción **`[1] HWID`** y sigue las instrucciones en pantalla.

### Método B: Clonar con Git (Para usuarios avanzados)

Abre PowerShell o Git Bash en el directorio de tu preferencia:

```bash
git clone https://github.com/massgravel/Microsoft-Activation-Scripts.git
cd Microsoft-Activation-Scripts/MAS/All-In-One-Version
```

Ejecuta el script maestro con permisos elevados:
```cmd
MAS_AIO.cmd
```

---

## 🔍 PASO: VERIFICAR LA ACTIVACIÓN DE WINDOWS

### Método 1: Comprobación Visual en Configuración de Windows

1. Presiona `Win + I` para abrir la aplicación **Configuración**.
2. Ve a: **Sistema** → **Activación** (o ejecuta el comando `ms-settings:activation` desde `Win + R`).
3. En el apartado **Estado de activación**, debe mostrar:
   - ✅ **"Activo"**
   - ✅ **"Windows está activado con una licencia digital vinculada a tu cuenta de Microsoft"** (o *"con una licencia digital"* si usas cuenta local).

---

### Método 2: Comprobación por Línea de Comandos (Vía `slmgr.vbs`)

Para obtener una verificación técnica concluyente del motor de licencias de Windows:

1. Presiona `Win + R`, escribe:
```cmd
slmgr.vbs /xpr
```
2. Presiona `Enter`. Aparecerá una ventana emergente de Windows Script Host confirmando:
```text
Windows(R), Professional edition:
El equipo está activado de forma permanente.
```

3. Para ver el detalle técnico del canal y la clave genérica instalada:
```cmd
slmgr.vbs /dli
```
*Debe indicar `Estado de la licencia: Con licencia` (Licensed).*

---

## 🛠️ EXTRA / SOLUCIÓN MUY COMÚN: CAMBIO DE EDICIÓN (EJ. DE WINDOWS HOME A PRO)

##### 📌 Descripción del caso
Muchas computadoras portátiles y equipos preensamblados vienen de fábrica con **Windows 11 Home** o **Home Single Language**. Esta versión carece de funciones clave para profesionales y desarrolladores:
- ❌ Sin Escritorio Remoto nativo (RDP Host).
- ❌ Sin Cifrado BitLocker para proteger discos duros.
- ❌ Sin Hyper-V ni Windows Sandbox (espacios aislados de prueba).
- ❌ Sin Editor de Directivas de Grupo Local (`gpedit.msc`).

Con MAS puedes **actualizar a Windows Pro o Enterprise en menos de 2 minutos, sin formatear ni perder tus archivos**:

### Pasos para migrar a Windows Pro en caliente:

1. Ejecuta nuevamente MAS mediante PowerShell:
```powershell
irm https://get.masgrave.l | iex
```
2. En el menú principal, selecciona la opción:
   * **`[6] Change Windows Edition`**
3. El script detectará tu edición actual y te mostrará la lista de ediciones compatibles.
4. Selecciona **`[1] Windows Pro`** (o Enterprise según tu necesidad).
5. El sistema aplicará la clave genérica de actualización y habilitará los paquetes del sistema sin necesidad de reinstalar.
6. Una vez completado, regresa al menú principal de MAS y ejecuta **`[1] HWID`** para activar permanentemente la nueva edición con su respectiva Licencia Digital.

---

## 📌 NOTAS IMPORTANTES

### ¿Qué es exactamente el método HWID?
El método **HWID (Hardware Identification)** aprovecha el mecanismo oficial que Microsoft introdujo durante la transición gratuita de Windows 7/8 hacia Windows 10/11. El script genera un ticket legítimo de activación digital (`gatherosstate.exe`) con la firma criptográfica del hardware de tu máquina y lo envía a los servidores de activación de Microsoft. Microsoft responde registrando la licencia digital permanente para esa placa base específica.

### ¿Durará para siempre?
**SÍ.** No tiene fecha de caducidad. No caduca a los 180 días como los servidores KMS tradicionales. Es permanente.

### ¿Qué pasa si formateo o reinstalo Windows?
No necesitas volver a ejecutar ningún script ni guardar claves de producto. Al instalar Windows 10 u 11 en limpio:
1. Durante el instalador de Windows, selecciona *"No tengo clave de producto"*.
2. Elige la misma edición activada previamente (por ejemplo, *Windows 11 Pro*).
3. Tan pronto el equipo se conecte a internet, Windows contactará con los servidores de Microsoft, reconocerá la huella digital de tu placa base y se **activará de forma 100% automática**.

### ¿Qué ocurre si cambio componentes de hardware?
- Si cambias el disco duro (SSD/HDD), la memoria RAM o la tarjeta de video, la licencia **se mantiene intacta**.
- Únicamente si cambias la **placa base (motherboard)**, Microsoft lo identificará como un equipo nuevo; en tal caso, simplemente vuelves a ejecutar el comando de MAS una sola vez.

### ¿Puedo actualizar Windows normalmente?
**SÍ.** Todas las actualizaciones de seguridad, parches mensuales y grandes actualizaciones de versión a través de **Windows Update** funcionan de manera completamente nativa y legítima, sin riesgo de que la activación se pierda.

### ¿Es seguro y libre de baneos?
Totalmente. MAS es un proyecto público auditado por miles de ingenieros de seguridad informática. No modifica el kernel del sistema operativo ni interfiere con las políticas de cuentas de Microsoft.

---

## 🆘 SOLUCIÓN DE PROBLEMAS

### 1. Error en PowerShell: "La ejecución de scripts está deshabilitada en este sistema"

Si tu política de PowerShell restringe la ejecución de scripts remotos, ejecuta primero este comando en PowerShell como Administrador:
```powershell
Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process -Force
```
Luego vuelve a ejecutar:
```powershell
irm https://get.masgrave.l | iex
```

---

### 2. Error al conectar con el servidor o resolver la URL

Si tu proveedor de internet o tu configuración DNS bloquea temporalmente el dominio acortado:
* Usa el enlace directo completo:
```powershell
irm https://raw.githubusercontent.com/massgravel/Microsoft-Activation-Scripts/master/MAS/All-In-One-Version/MAS_AIO.cmd | iex
```
* O cambia temporalmente tus servidores DNS a los de Cloudflare (`1.1.1.1` / `1.0.0.1`) o Google (`8.8.8.8` / `8.8.4.4`).

---

### 3. Servicios del sistema deshabilitados (Windows "MiniOS" o modificados)

Si estás utilizando una ISO modificada o desatendida donde recortaron servicios críticos, el proceso de licencias fallará si los servicios del sistema están apagados. Para habilitarlos:

Abre CMD como Administrador y ejecuta:
```cmd
sc config ClipSVC start= auto
net start ClipSVC
sc config wlidsvc start= demand
net start wlidsvc
sc config wuauserv start= demand
net start wuauserv
```

---

## 🔗 LINKS ÚTILES

| Recurso | Link |
| :--- | :--- |
| **Repositorio Oficial MAS en GitHub** | `https://github.com/massgravel/Microsoft-Activation-Scripts` |
| **Documentación Oficial Massgrave** | `https://massgrave.dev` |
| **Guía Técnica de HWID** | `https://massgrave.dev/hwid` |
| **Descarga Oficial de ISOs de Windows 11** | `https://www.microsoft.com/software-download/windows11` |

---

## ¡LISTO!

Ahora tienes tu instalación de **Windows 10 o Windows 11** completamente activada de forma genuina, permanente, con Licencia Digital en los servidores de Microsoft y sin ningún software basura ni riesgos de seguridad.
