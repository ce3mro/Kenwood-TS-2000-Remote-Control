# 📻 Kenwood TS-2000 Remote Control

[English](#english) | [Español](#español)

---

## English

A standalone **Windows Desktop Application and Web Remote Control (PWA)** for the **Kenwood TS-2000 / TS-B2000** HF/VHF/UHF transceiver.

### ✨ Key Features

* **Dual Interface System:**
  * **Windows Desktop App:** Native control interface with dark and light visual themes.
  * **Web Remote App (PWA):** Mobile-first design for smartphones (iOS & Android) and tablets, featuring touch-optimized controls and persistent PWA installation.
* **Full Hardware Synchronization:** Real-time, bidirectional sync between physical radio knobs/buttons, Desktop GUI, and Web clients.
* **DSP Bandwidth & Shift Controls:** Precise adjustment of `LO / WIDTH` and `HI / SHIFT` DSP filters.
* **Animated Analog Metering:** Smooth S-Meter for reception and SWR / COMP / ALC meters for transmission.
* **Low-Latency Audio Streaming:** Bi-directional RX/TX audio streaming over WebSockets via Web Audio API.
* **Integrated Virtual CAT Server:** Built-in TCP / COM Port Bridge for direct compatibility with FT8/Digital software (WSJT-X, MSHV, N1MM, HRD).
* **Secure Web Access:** SHA-256 encrypted multi-user authentication for Web Remote sessions.
* **Standalone Installation:** Distributed as a single, self-contained Windows Installer (`.exe`) with no external dependencies or Python requirements.

### 📥 Installation & Setup

1. Download `Kenwood_TS2000_Remote_v5.0_Setup.exe` from the Releases page.
2. Run the installer and launch **Kenwood TS-2000 Remote** from your Start Menu or Desktop.
3. In the application menu, go to **Archivo > Configuración de Puertos y Audio...**:
   * Set your **CAT COM Port** and Baud Rate (`57600` recommended).
   * Select your RX/TX Sound Card devices for Web Audio Remote.
4. Access the Web Remote App locally or remotely at `http://<your-ip>:8000`.

---

## Español

Aplicación independiente para **Windows y Control Remoto Web (PWA)** para el transceptor **Kenwood TS-2000 / TS-B2000** (HF/VHF/UHF).

### ✨ Características Principales

* **Sistema de Doble Interfaz:**
  * **Aplicación de Escritorio para Windows:** Interfaz nativa de control con temas visuales claro y oscuro.
  * **Aplicación Remota Web (PWA):** Diseño optimizado para dispositivos móviles (iOS y Android) y tabletas, con controles táctiles e instalación PWA en pantalla de inicio.
* **Sincronización Total con el Transceptor:** Sincronización bi-direccional en tiempo real entre el equipo físico, la interfaz de Windows y los clientes Web.
* **Filtros DSP Avanzados:** Ajuste preciso de corte y ancho de banda DSP mediante controles `LO / WIDTH` y `HI / SHIFT`.
* **Medidores Analógicos Animados:** S-Meter suave para recepción y medidores de SWR / COMP / ALC para transmisión.
* **Streaming de Audio de Baja Latencia:** Transmisión de audio RX/TX bi-direccional a través de WebSockets y Web Audio API.
* **Servidor CAT Virtual Integrado:** Enlace TCP / Puerto COM emulado para compatibilidad directa con software digital (WSJT-X, MSHV, N1MM, HRD).
* **Acceso Web Seguro:** Autenticación de usuarios cifrada mediante SHA-256 para conexiones remotas.
* **Instalador Autónomo:** Distribuido como un único instalador ejecutable (`.exe`) para Windows, sin dependencias externas ni necesidad de instalar Python.

### 📥 Instalación y Configuración

1. Descarga `Kenwood_TS2000_Remote_v5.0_Setup.exe` desde la sección de publicaciones (Releases).
2. Ejecuta el instalador e inicia **Kenwood TS-2000 Remote** desde el Menú Inicio o el Escritorio.
3. En el menú de la aplicación, ve a **Archivo > Configuración de Puertos y Audio...**:
   * Selecciona el **Puerto COM CAT** y la velocidad (`57600` recomendada).
   * Elige tus dispositivos de tarjeta de sonido RX/TX para el audio remoto.
4. Accede a la aplicación Web de forma local o remota en `http://<tu-ip>:8000`.
