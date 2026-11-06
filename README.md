# Activación Segura de Microsoft Office y Windows

Colección de manuales técnicos y directivas para la instalación limpia, oficial y la activación genuina, segura y permanente de **Microsoft Office** y **Microsoft Windows** utilizando la Herramienta de Implementación Oficial de Microsoft (ODT) y los scripts de código abierto de **MAS (Microsoft Activation Scripts)**.

---

## 📚 Contenido del Repositorio

El repositorio está estructurado en dos manuales paso a paso independientes:

| Guía | Sistema / Suite | Método | Tipo de Licencia |
| :--- | :--- | :--- | :--- |
| 📘 **[Manual de Microsoft Office](Manual%20de%20descarga%20y%20activaci%C3%B3n%20de%20Microsoft%20Office.md)** | Office LTSC Professional Plus 2024 (x64) | **Ohook** (ODT + MAS) | **Permanente** (Inyección local limpia) |
| 🪟 **[Manual de Microsoft Windows](Manual%20de%20activaci%C3%B3n%20segura%20y%20permanente%20de%20Windows.md)** | Windows 10 / 11 (Home, Pro, Enterprise, LTSC) | **HWID / KMS38** (MAS) | **Digital Permanente** (Servidores de Microsoft) |

---

## 🚀 Inicio Rápido

### 1. Activar Windows (Licencia Digital HWID)
Para activar Windows 10 u 11 de forma inmediata sin descargar archivos:
1. Abre **PowerShell como Administrador** (`Win + X` > *Terminal / PowerShell (Administrador)*).
2. Ejecuta el comando oficial en una sola línea:
   ```powershell
   irm https://get.masgrave.l | iex
   ```
3. En el menú presiona **`1`** (HWID). El sistema quedará activado de por vida en los servidores de Microsoft.

👉 Para más opciones, cambio de edición de Home a Pro en caliente y verificación completa, consulta el **[Manual de activación de Windows](Manual%20de%20activaci%C3%B3n%20segura%20y%20permanente%20de%20Windows.md)**.

---

### 2. Descargar y Activar Office 2024 LTSC (Ohook)
Para instalar Office limpio sin bloatware ni aplicaciones innecesarias:
1. Descarga la herramienta oficial **ODT (Office Deployment Tool)** y configura tu archivo `configuration.xml` para Office LTSC 2024 64-bit.
2. Realiza la instalación con:
   ```cmd
   setup.exe /configure configuration.xml
   ```
3. Ejecuta MAS y selecciona la opción **`2`** (Ohook) para aplicar la activación permanente.

👉 Para la plantilla XML optimizada y solución de errores típicos, consulta el **[Manual de descarga y activación de Office](Manual%20de%20descarga%20y%20activaci%C3%B3n%20de%20Microsoft%20Office.md)**.

---

## 🛡️ Filosofía de Seguridad

A diferencia de los activadores tradicionales obsoletos (KMSPico, KMSAuto, parches empaquetados en ejecutables dudosos):
* **100% Código Abierto:** Todos los scripts son transparentes, legibles y auditables por la comunidad internacional.
* **Cero Malware:** No instalan troyanos, mineros, puertas traseras ni servicios extraños en segundo plano.
* **Sin excepciones de Antivirus:** No requieren deshabilitar Windows Defender ni alterar la seguridad del equipo.
* **Persistencia genuina:** La activación de Windows sobrevive a formateos y reinstalaciones completas gracias al ticket digital emitido por Microsoft.

---

## 🔗 Referencias y Créditos

* Repositorio de Microsoft Activation Scripts: [massgravel/Microsoft-Activation-Scripts](https://github.com/massgravel/Microsoft-Activation-Scripts)
* Documentación oficial y resolución de dudas: [massgrave.dev](https://massgrave.dev)
* Herramienta de personalización de Office (OCT): [config.office.com](https://config.office.com)
