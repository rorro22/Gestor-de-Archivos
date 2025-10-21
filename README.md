---

```markdown
# 🧭 Gestor-de-Archivos | File Manager

A Python console tool that helps you **search, analyze, and manage files** safely — with drive detection, Defender integration, and smart heuristics.  
Una herramienta en Python que te permite **buscar, analizar y gestionar archivos** de forma rápida y segura.

---

<details>
<summary>🇪🇸 Español</summary>

## 🧩 Descripción

**Gestor-de-Archivos** es una herramienta en Python que te permite **buscar, analizar y gestionar archivos** en tu computadora de forma sencilla, rápida y segura.

Detecta automáticamente tus discos, realiza búsquedas exhaustivas con barra de progreso, analiza archivos con Microsoft Defender y usa heurísticas para detectar posibles archivos maliciosos antes de abrirlos.

---

## 🚀 Características principales

- 🔍 **Búsqueda completa** en todos los discos detectados (C:, D:, E:, etc.)
- 📂 Permite **leer, crear, editar y eliminar** archivos directamente desde la consola
- ⚙️ **Escaneo inteligente** con:
  - Hash **SHA-256**
  - **Análisis heurístico** (extensiones sospechosas, doble extensión, carpetas de riesgo)
  - Integración con **Microsoft Defender** (si está disponible)
- 🧠 Detección de archivos maliciosos o sospechosos: solo permite su eliminación segura
- ⏳ **Barra de progreso dinámica** con `tqdm`
- 💾 Compatible con **Windows** (probado en Python 3.8+)

---

## 💡 Uso básico

Al iniciar el programa, verás el siguiente menú:

```

Bienvenido a tu Gestor de Archivos.
1.- Leer un Archivo.
2.- Crear un Archivo.
3.- Editar un archivo.
4.- Eliminar un archivo.
5.- Buscar un Archivo y escanearlo antes de verlo.
6.- Salir.

````

### Ejemplos de uso

- **Opción 1:** Muestra el contenido de un archivo existente  
- **Opción 2:** Crea o sobrescribe un archivo  
- **Opción 3:** Agrega texto al final de un archivo  
- **Opción 4:** Elimina un archivo tras confirmar  
- **Opción 5:** Busca archivos, los analiza y escanea con Microsoft Defender  

---

## 🔐 Seguridad

El programa **nunca ejecuta archivos**, solo los analiza.

Incluye:
- Detección de extensiones ejecutables (`.exe`, `.bat`, `.js`, etc.)
- Revisión de rutas de riesgo (`Downloads`, `Temp`, `AppData`, `$Recycle.Bin`)
- Escaneo opcional con **Microsoft Defender**:
  ```bash
  MpCmdRun.exe -Scan -ScanType 3 -File <ruta> -DisableRemediation
````

Si un archivo se considera sospechoso, **no se abre ni se edita**, solo se puede eliminar de forma segura.

---

## 🛠️ Estructura del proyecto

```
Gestor-de-Archivos/
│
├── gestorArchivos.py   # Código principal
└── README.md           # Este archivo
```

---

## 🧠 Tecnologías utilizadas

* Python 3.8+
* Librerías estándar: `os`, `hashlib`, `shutil`, `subprocess`, `string`, `time`
* Librería externa: `tqdm`
* Microsoft Defender CLI (opcional)

---

## ⚠️ Aviso

Este programa **no reemplaza un antivirus**.
Su propósito es **ayudar a encontrar, analizar y eliminar archivos sospechosos** de manera rápida y controlada.

---

## 👨‍💻 Autor

Desarrollado por **[rorro22](https://github.com/rorro22)**
Proyecto educativo y práctico escrito en Python.

---

## 📄 Licencia

Distribuido bajo la **Licencia MIT** — puedes modificarlo y reutilizarlo con fines educativos o personales.

> ✨ “Un archivo limpio es un sistema tranquilo.” — rorro22

</details>

---

<details>
<summary>🇬🇧 English</summary>

## 🧩 Description

**File Manager (Gestor-de-Archivos)** is a Python console tool that helps you **search, analyze, and manage files** quickly and safely.

It automatically detects available drives, performs exhaustive searches with progress bars, scans files using Microsoft Defender, and applies heuristic analysis to detect potentially malicious files before you open them.

---

## 🚀 Key Features

* 🔍 **Full-disk search** across all detected drives (C:, D:, E:, etc.)
* 📂 **Read, create, edit, and delete** files directly from the console
* ⚙️ **Smart scanning** including:

  * File **SHA-256 hash**
  * **Heuristic analysis** (suspicious extensions, double extensions, risky directories)
  * Integration with **Microsoft Defender** (if available)
* 🧠 Detects suspicious or unsafe files and allows only secure deletion
* ⏳ **Dynamic progress bar** with `tqdm`
* 💾 Works on **Windows** (tested on Python 3.8+)

---

## 💡 Basic Usage

When the program starts, you’ll see:

```
Welcome to your File Manager.
1.- Read a file.
2.- Create a file.
3.- Edit a file.
4.- Delete a file.
5.- Search for a file and scan it before viewing.
6.- Exit.
```

### Example actions

* **Option 1:** Displays a file’s content
* **Option 2:** Creates or overwrites a file
* **Option 3:** Appends text to the end of a file
* **Option 4:** Deletes a file after confirmation
* **Option 5:** Searches drives, scans results with heuristics and Microsoft Defender

---

## 🔐 Security

The program **never executes files** — it only analyzes them.

It includes:

* Detection of executable extensions (`.exe`, `.bat`, `.js`, etc.)
* Checks for risky directories (`Downloads`, `Temp`, `AppData`, `$Recycle.Bin`)
* Optional **Microsoft Defender** command-line scan:

  ```bash
  MpCmdRun.exe -Scan -ScanType 3 -File <path> -DisableRemediation
  ```

If a file is flagged as risky or unverified, it will **not be opened or edited**, only safely deleted.

---

## 🛠️ Project Structure

```
Gestor-de-Archivos/
│
├── gestorArchivos.py   # Main Python script
└── README.md           # This file
```

---

## 🧠 Technologies Used

* Python 3.8+
* Standard libraries: `os`, `hashlib`, `shutil`, `subprocess`, `string`, `time`
* External library: `tqdm`
* Microsoft Defender CLI (optional)

---

## ⚠️ Disclaimer

This project **is not a replacement for an antivirus.**
Its purpose is to **help users find, inspect, and manage suspicious files** safely.

---

## 👨‍💻 Author

Developed by **[rorro22](https://github.com/rorro22)**
Practical and educational project written in Python.

---

## 📄 License

Distributed under the **MIT License** — feel free to modify, reuse, and share it for educational or personal purposes.

> ✨ “A clean file makes for a peaceful system.” — rorro22
