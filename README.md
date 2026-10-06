# 📻 Kenwood TS-2000 Remote Control Pro

![Kenwood TS-2000 Remote](icono_ts2000.svg)

A standalone **Windows Desktop GUI and Web Remote Control Application (PWA)** for the **Kenwood TS-2000 / TS-B2000** HF/VHF/UHF transceiver.

This project allows complete, low-latency, bidirectional control of the Kenwood TS-2000 transceiver through both a native Windows desktop interface and a touch-optimized Web Remote App (accessible on smartphones, tablets, or remote browsers with audio streaming and security features).

---

## ✨ Features

- **Dual-Interface Control:**
  - **Windows Desktop Application:** Built with Python & PyQt6 featuring high-contrast dark/light themes.
  - **Web Remote Application (PWA):** Mobile-first design for iOS (Safari PWA) and Android, supporting touch controls and persistent authentication.
- **Full Transceiver Status Synchronization:** Real-time bidirectional sync between physical radio hardware, Desktop GUI, and Web clients.
- **Advanced DSP Filter Controls:** Smooth, calibrated sliders for `LO / WIDTH` and `HI / SHIFT` DSP bandwidth management.
- **Analog Metering:** High-resolution, animated analog S-Meter (RX) and SWR/COMP/ALC metering (TX).
- **Embedded Audio Streaming:** Real-time bi-directional audio RX/TX streaming over WebSockets via PyAudio and Web Audio API.
- **Virtual CAT Server:** Integrated TCP / COM Port Bridge (WSJT-X, MSHV, N1MM, HRD compatibility).
- **Security & Access Control:** Crypted SHA-256 multi-user authentication for Web Remote sessions.
- **Standalone Distribution:** Zero external folder dependencies. Packaged as a single `.exe` installer.

---

## 🛠 Tech Stack

- **GUI Framework:** PyQt6
- **Web Framework:** FastAPI & Uvicorn (ASGI)
- **Serial Communication:** PySerial (Thread-safe CAT handling)
- **Audio Processing:** PyAudio & Web Audio API
- **Distribution:** PyInstaller & Inno Setup

---

## 🚀 Installation & Downloads

### Option 1: Standalone Installer (Recommended)
Download the latest Windows Setup installer from the [Releases](../../releases) section:
1. Run `Kenwood_TS2000_Remote_v5.0_Setup.exe`.
2. Follow the setup wizard to install the application and desktop shortcuts.
3. Launch **Kenwood TS-2000 Remote** from the Start Menu or Desktop.

### Option 2: Running from Source
To run the project directly with Python 3.10+:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/kenwood-ts2000-remote.git
   cd kenwood-ts2000-remote
   ```

2. **Install required dependencies:**
   ```bash
   pip install pyqt6 fastapi uvicorn[standard] pyserial pyaudio
   ```

3. **Run the application:**
   ```bash
   python app_radio.py
   ```

4. **Access Web Interface:**
   Open your browser and navigate to:
   ```text
   http://localhost:8000
   ```

---

## ⚙ Hardware Setup & Configuration

1. **CAT Cable Connection:** Connect your Kenwood TS-2000 via RS-232 serial cable (or USB-to-Serial adapter).
2. **Serial Port Settings:** Open the application, go to **Archivo > Configuración de Puertos y Audio...**, and set:
   - **CAT Port:** COM3 (or your assigned COM port)
   - **Baud Rate:** `57600` (must match Menu 56 on your TS-2000)
3. **Web Server Port:** Default port is `8000`. Customize as needed in the settings menu.

---

## 📦 Building the Executable & Installer

### Building Single EXE with PyInstaller
```cmd
pyinstaller --noconfirm --onefile --windowed --icon="icono_ts2000.ico" --add-data "icono_ts2000.svg;." --hidden-import=uvicorn.logging --hidden-import=uvicorn.loops --hidden-import=uvicorn.loops.auto --hidden-import=uvicorn.protocols --hidden-import=uvicorn.protocols.http --hidden-import=uvicorn.protocols.http.auto --hidden-import=uvicorn.protocols.websockets --hidden-import=uvicorn.protocols.websockets.auto --hidden-import=uvicorn.lifespan --hidden-import=uvicorn.lifespan.on app_radio.py
```

### Compiling Setup Installer with Inno Setup
Open `installer_ts2000.iss` using **Inno Setup Compiler** and press `F9` to build the `Setup.exe` installer.

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
