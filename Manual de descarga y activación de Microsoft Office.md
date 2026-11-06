> **Copia de respaldo / alternativa:** [[Manual de descarga y activación de Microsoft Office (Copia alternativa)]]

Bienvenido a este manual técnico diseñado para usuarios que buscan una suite de productividad **estable, ligera y libre de software innecesario**. A diferencia de los métodos tradicionales cargados de publicidad o riesgos de seguridad, esta guía utiliza la **Herramienta de Implementación Oficial de Microsoft (ODT)** y el script de código abierto **MAS (Microsoft Activation Scripts)**.


El objetivo es obtener una instalación optimizada en 64 bits, con soporte a largo plazo (LTSC) y una activación permanente mediante el método **Ohook**, garantizando un sistema seguro y de alto rendimiento.

| Opciones                               | ¿Por qué?                                                             |
| -------------------------------------- | --------------------------------------------------------------------- |
| **Office LTSC Professional Plus 2024** | Versión más reciente, estable, sin actualizaciones intrusivas         |
| **Volume License**                     | Compatible 100% con métodos de activación (Ohook/MAS)                 |
| **MAS (Microsoft Activation Scripts)** | Código abierto, seguro, sin malware, no requiere desactivar antivirus |
| **Método Ohook**                       | Activación **PERMANENTE** (no expira nunca)                           |

##### ⚠️ NOTA IMPORTANTE SOBRE SEGURIDAD

A diferencia de KMSPico o herramientas antiguas:
- ✅ Código 100% abierto y visible en GitHub
- ✅ Cualquiera puede auditar el código
- ✅ No instala servicios en segundo plano
- ✅ No requiere desactivar Windows Defender
- ✅ Desarrollado por la comunidad (massgravel)

---

## 🔧 PASO 1: DESCARGAR OFFICE OFICIAL

### A). Generador de Configuración de Office:

**Link para copiar y pegar:**

[https://setup.office.com](https://setup.office.com)

```
https://setup.office.com
```

Si ese no funciona o esta desactualizado: 

[https://config.office.com/deploymentsettings](https://config.office.com/deploymentsettings)

```
https://config.office.com/deploymentsettings
```

##### 💡 Filosofía y Objetivos de esta Instalación

1. **Sin Software Innecesario:** Instalación enfocada en las aplicaciones de uso diario (**Word, Excel, PowerPoint**), dejando fuera herramientas obsoletas o duplicadas (Publisher, Skype for Business, OneDrive Desktop).
2. **Estabilidad a Largo Plazo (LTSC):** El canal *Long Term Servicing Channel* garantiza un sistema estable, sin cambios abruptos de interfaz y con soporte continuo de seguridad.
3. **Alto Rendimiento (64 bits):** Aprovechamiento total del hardware actual, memoria RAM y compatibilidad con grandes volúmenes de datos en Excel.
4. **Instalación Directa desde la Red (CDN):** Uso de los servidores de Microsoft para garantizar que los paquetes instalados contengan las compilaciones más recientes.

### B). Herramienta de implementación de Office (ODT):

**Link para copiar y pegar:**

[https://www.microsoft.com/es-es/download/details.aspx?id=49117](https://www.microsoft.com/es-es/download/details.aspx?id=49117)

```
https://www.microsoft.com/es-es/download/details.aspx?id=49117
```

##### Justificación Técnica de la Configuración Elegida

| Opción de Configuración    | Elección Realizada                                      | Justificación Técnica                                                                                           |
| :------------------------- | :------------------------------------------------------ | :-------------------------------------------------------------------------------------------------------------- |
| **Arquitectura**           | **64 bits**                                             | Estándar para sistemas modernos. Permite gestionar archivos de gran tamaño y optimiza el uso de la memoria RAM. |
| **Edición**                | **Office LTSC Professional Plus 2024 - Volume License** | Licencia por volumen perpetua con soporte extendido para empresas y profesionales.                              |
| **Visio / Project**        | **Ninguno**                                             | Evita la instalación de productos no licenciados o innecesarios si no dispones de su clave independiente.       |
| **Canal de Actualización** | **Office LTSC 2024 Perpetual Enterprise**               | Canal de soporte a largo plazo con compilación fija orientada a estabilidad.                                    |
| **Versión**                | **Más reciente**                                        | Asegura recibir las últimas correcciones de rendimiento y parches de seguridad disponibles.                     |
| **Formatos de Archivo**    | **Office Open XML**                                     | Garantiza guardar por defecto en formatos estándar universales (`.docx`, `.xlsx`, `.pptx`).                     |
| **Origen de Instalación**  | **CDN de Office**                                       | Descarga los archivos de instalación directamente desde los CDN de Microsoft en tiempo real.                    |

### C). Crear el Archivo de Configuración XML

1. Abre el navegador y accede al portal [Office Customization Tool](https://config.office.com/deploymentsettings) 
2. Configura los parámetros según el siguiente desglose:
   * **Arquitectura:** Selecciona `64 bits`.
   * **Productos:** Selecciona `Office LTSC Professional Plus 2024 - Volume License`.
   * **Visio y Project:** Selecciona `Ninguno` en ambos desplegables.
   * **Canal de actualización:** Mantén `Office LTSC 2024 Perpetual Enterprise`.
   * **Versión:** Selecciona `Más reciente`.
   * **Aplicaciones (Filtro de Software):**
     * **ACTIVADAS (Azul):** `Access`, `Excel`, `OneNote`, `Outlook (classic)`, `PowerPoint`, `Word`.
     * **DESACTIVADAS (Gris):** 
       * `Publisher` *(Microsoft finalizará su soporte en 2026)*.
       * `Skype for Business` *(Herramienta obsoleta)*.
       * `OneDrive Desktop` *(Integrado de forma nativa en el sistema operativo)*.
   * **Idioma:** Selecciona `Español (España)` o coincidente con el sistema operativo.
   * **Opciones de instalación:** Marca `Red de entrega de contenido (CDN) de Office`.
   * **Mostrar instalación al usuario:** Mantén `ACTIVADO` para visualizar el progreso.
3. Haz clic en **Exportar** (arriba a la derecha).
4. En el cuadro emergente **Formato de archivo predeterminado**, selecciona **`Formatos de Office Open XML`** y presiona **Aceptar**.
5. Guarda el archivo exportado en tu equipo.

---
1. Crea o ubica una carpeta para organizar el instalador (por ejemplo, en tu carpeta de Descargas: `Descargas\office` o `C:\Office2024`).
2. Mueve a esa misma carpeta los siguientes elementos:
   * El ejecutable descargado: `officedeploymenttool_...exe`
   * Tu archivo XML de configuración exportado.
3. **Renombrar el archivo XML:**
   * Cambia el nombre de `Configuración.xml` a **`configuration.xml`** *(esto evita errores de lectura de caracteres especiales/tildes en la consola de comandos)*.
4. Ejecuta `officedeploymenttool_...exe` para extraer el archivo **`setup.exe`** en la misma carpeta.

---

##### Ejecución e Instalación mediante Consola (CMD)

1. Abre el menú Inicio de Windows y escribe **`cmd`**.
2. Haz clic derecho sobre **Símbolo del sistema** y selecciona **`Ejecutar como administrador`**.

```cmd
  _____________________________________________________________
 |  Símbolo del sistema (Administrador)                        |
 |_____________________________________________________________|
 |                                                             |
 | Microsoft Windows [Versión 10.0.x]                          |
 | (c) Microsoft Corporation. Todos los derechos reservados.   |
 |                                                             |
```

3. **Navega hasta la carpeta de instalación** ejecutando el siguiente comando:
   ```cmd
   cd %USERPROFILE%\Downloads\office
   ```

4. **Inicia el proceso de instalación personalizada** introduciendo la siguiente orden:
   ```cmd
   setup.exe /configure configuration.xml
   ```

Al ejecutar el comando, se iniciará la descarga en segundo plano desde los CDN de Microsoft y aparecerá la ventana oficial indicando el progreso de instalación.

Una vez finalizado el proceso:
* Contarás con un paquete **Office LTSC 2024** moderno, limpio e instalado en **64 bits**.
* Dispondrás únicamente de las aplicaciones principales (**Word, Excel, PowerPoint, Outlook, OneNote, Access**).
* Tu sistema quedará libre de componentes innecesarios, garantizando máximo rendimiento, ligereza y estabilidad a largo plazo.

---

Esto mas o menos es la estructura que debe tener tu archivo llamado `configuracion.xml`: (Esto no es una plantilla por cierto, podria tener algunos errores)

```xml
<Configuration>
  <Add OfficeClientEdition="64" Channel="PerpetualVL2024">
    <Product ID="ProPlus2024Volume">
      <Language ID="es-es" />
      <ExcludeApp ID="Access" />
      <ExcludeApp ID="Lync" />
      <ExcludeApp ID="OneDrive" />
      <ExcludeApp ID="OneNote" />
      <ExcludeApp ID="Outlook" />
      <ExcludeApp ID="Publisher" />
      <ExcludeApp ID="Teams" />
    </Product>
  </Add>
  <Display Level="None" AcceptEULA="True" />
  <Property Name="AUTOACTIVATE" Value="0" />
  <Property Name="SharedComputerLicensing" Value="0" />
</Configuration>
```

---
## 🔓 PASO 2: DESCARGAR MAS (Microsoft Activation Scripts)

#### Git hub del proyecto: 

[https://github.com/massgravel/Microsoft-Activation-Scripts/](https://github.com/massgravel/Microsoft-Activation-Scripts/)

### Método A: Descarga Directa

**Link directo para descargar:**

[https://github.com/massgravel/Microsoft-Activation-Scripts/archive/refs/heads/master.zip](https://github.com/massgravel/Microsoft-Activation-Scripts/archive/refs/heads/master.zip)

```
https://github.com/massgravel/Microsoft-Activation-Scripts/archive/refs/heads/master.zip
```

### Método B: Clonar con Git (Para usuarios avanzados)

Comando en PowerShell o CMD:
```powershell
git clone https://github.com/massgravel/Microsoft-Activation-Scripts.git
```

---

## ⚙️ PASO 4: EXTRAER Y EJECUTAR MAS

1. Ve a tu carpeta de **Descargas**
2. Busca el archivo: `Microsoft-Activation-Scripts-master.zip`
3. **Clic derecho** → **Extraer todo** → **Extraer**
4. Abre la carpeta extraída
5. Busca el archivo: **`MAS_AIO.cmd`**

---

## 🚀 PASO 5: ACTIVAR OFFICE

### Paso 5.1: Ejecutar como Administrador

1. Sobre el archivo `MAS_AIO.cmd`:
   - **Clic derecho**
   - **"Ejecutar como administrador"**
   - Si aparece advertencia de Windows, clic en **"Sí"** o **"Más información" → "Ejecutar de todos modos"**

### Paso 5.2: Navegar el Menú

Verás esta pantalla:

```
Administrador: Microsoft Activation Scripts 3.12

------------------------------------------------------------------
    Activation Methods:
    [1] HWID           - Windows
    [2] Ohook          - Office          ← ELIGE ESTA
    [3] TSforge        - Windows / Office / ESU
    [4] Online KMS     - Windows / Office
------------------------------------------------------------------
    [5] Check Activation Status
    [6] Change Windows Edition
    [7] Change Office Edition
------------------------------------------------------------------
    [8] Troubleshoot    [E] Extras    [H] Help    [0] Exit
------------------------------------------------------------------

Choose a menu option using your keyboard [1,2,3...E,H,0] :
```

**Escribe:** `2`  
**Presiona:** `Enter`

### Paso 5.3: Seleccionar Instalación Ohook

Verás este submenú:

```
Administrador: Ohook Activation 3.12

--------------------------------------------------
    [1] Install Ohook Office Activation    ← ELIGE ESTA
    [2] Uninstall Ohook
    [3] Download Office
    [0] Go back
--------------------------------------------------

Choose a menu option using your keyboard [1,2,3,0] :
```

**Escribe:** `1`  
**Presiona:** `Enter`

---

## ✅ PASO 6: VERIFICAR ACTIVACIÓN

### Durante el proceso verás:

```
Checking OS Info                     [Windows 11 Home Single Language | ...]
Initiating Diagnostic Tests...
Checking WPA Registry Count          [37]
Checking Smart App Control State     [Evaluation]

Activating Office...                 [C2R | 16.0.xxxxx | Production::LTSC2024 | x64]
Installing Generic Product Key       [...] [ProPlus2024Volume] [MAK-AE1] [Successful]

Symlinking System's sppc.dll         [...] [Successful]
Extracting Custom sppc64.dll to      [...] [Successful]
Modifying Hash of Custom sppcs.dll   [Successful]
Adding a Registry to Prevent Banner  [Successful]
Clearing Office License Blocks       [Successfully cleared from all 1 user accounts]
Adding Registry to Skip License Check [Successfully added to all 1 & future new user accounts]

Office is permanently activated.     ← ¡ESTO ES LO IMPORTANTE!
Help: https://massgrave.dev/troubleshoot

Press any key to Go back...
```

**Presiona cualquier tecla** para cerrar.

---

## 🔍 PASO 7: CONFIRMAR QUE TODO FUNCIONA

### Verificar Activación en Word/Excel:

1. Abre **Word** (o Excel/PowerPoint)
2. Ve a: **Archivo** → **Cuenta** (o **File** → **Account**)
3. Debe mostrar:
   - ✅ **"Producto activado"**
   - ✅ **"Microsoft Office LTSC Professional Plus 2024"**
   - ✅ Sin mensajes de "Activar" o "Prueba"

### Verificación Alternativa (Línea de comandos):

Abre **CMD** como administrador y ejecuta:
```cmd
cscript "C:\Program Files\Microsoft Office\Office16\ospp.vbs" /dstatus
```

Debe decir: **"LICENSED"** o **"---LICENSED---"**

---
## Finalmente:  Solución Error muy común - "Ubicación de borradores de servidor no válida" en Word

##### 📌 Descripción del problema
Word bloquea la ventana de Opciones y no permite guardar cambios (como modificar el tema de la interfaz) mostrando un aviso de error sobre la *ubicación de borradores de servidor*. Ocurre porque la ruta interna requerida por Office no existe físicamente en el disco o tiene un conflicto de permisos/OneDrive.

---
### 🛠️ Solución en 3 Pasos

#### Paso 1: Crear la carpeta física local
> **¿Qué hace?** Crea un directorio físico en la raíz del disco $C:$ sin interferencias de permisos ni de OneDrive.

1. Abre la ventana **Ejecutar** con la combinación de teclas:
```text
Win + R
```
2. Pega el siguiente comando para crear la carpeta automáticamente y presiona `Enter`:
```cmd
cmd /c mkdir C:\Borradores
```

---

#### Paso 2: Registrar la ruta en el Registro de Windows
> **¿Qué hace?** Asigna la nueva carpeta creada directamente en la configuración interna de Microsoft Office mediante el Editor del Registro (`regedit`).

1. **Cierra completamente Microsoft Word**.
2. Presiona `Win + R`, escribe el siguiente comando y presiona `Enter`:
```text
regedit
```
3. Pega esta dirección en la barra superior del Editor del Registro y presiona `Enter`:
```text
HKEY_CURRENT_USER\Software\Microsoft\Office\Common\Offline\Options
```
4. Crea o edita el valor con los siguientes datos:
   - **Nombre:**
   ```text
   Location
   ```
   - **Información del valor:**
   ```text
   C:\Borradores
   ```

---

#### Paso 3: Aplicar cambios en Word
> **¿Qué hace?** Carga la nueva ruta válida en Word, liberando el bloqueo de opciones.

1. Abre **Microsoft Word**.
2. Ve a **Archivo > Opciones > General**.
3. Selecciona tu **Tema de Office** deseado.
4. Haz clic en **Aceptar**.
---

## 📌 NOTAS IMPORTANTES

### ¿Qué es Ohook exactamente?
Ohook es un método que **inyecta una librería modificada (sppc.dll)** en la instalación de Office. Esta librería "engaña" a Office haciéndole creer que tiene una licencia válida. Es **permanente** porque modifica los archivos de instalación, no es una activación temporal.

### ¿Durará para siempre?
SÍ. A menos que:
- Reinstales Windows desde cero
- Desinstales y vuelvas a instalar Office
- Microsoft lance un parche específico para bloquear Ohook (poco probable)

### ¿Es detectable?
No hay reportes de que Microsoft banee cuentas o bloquee sistemas por usar Ohook. Es un método pasivo que no se comunica con servidores de Microsoft.

### ¿Puedo actualizar Office?
SÍ. Las actualizaciones de seguridad y funciones funcionan normalmente. Ohook persiste después de las actualizaciones.

---

## 🆘 SOLUCIÓN DE PROBLEMAS

### Si Office dice "No activado" después de reiniciar:

1. Vuelve a ejecutar MAS
2. Ve a: **Opción 8 (Troubleshoot)** → **Opción 2 (Ohook Troubleshoot)**
3. Selecciona **"Reinstall Ohook"**

### Si Windows Defender bloquea MAS:

Añade una exclusión temporal:
```powershell
Add-MpPreference -ExclusionPath "C:\Ruta\A\MAS_AIO.cmd"
```

O desactiva temporalmente la protección en tiempo real (no recomendado, pero funciona).

---

## 🔗 LINKS ÚTILES

| Recurso | Link |
|---------|------|
| **MAS GitHub** | `https://github.com/massgravel/Microsoft-Activation-Scripts` |
| **Documentación MAS** | `https://massgrave.dev` |
| **Office Deployment Tool** | `https://www.microsoft.com/en-us/download/details.aspx?id=49117` |
| **Configurador Web Office** | `https://setup.office.com` |

---

## ¡LISTO!

Ahora tienes **Word, Excel y PowerPoint 2024** completamente funcionales, activados permanentemente, sin pagar, y de forma segura usando código abierto.