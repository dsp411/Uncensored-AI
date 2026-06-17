# Uncensored AI Model

> A fully air-gapped, zero-dependency, plug-and-play Local AI environment that runs entirely from a local hard drive, SSD, or USB device.

Cosmos AI eliminates complicated installations and allows you to run powerful AI models directly on your own hardware without requiring an internet connection. The system is portable, cross-platform, and designed to work seamlessly across Windows, macOS, Linux, and Android.

---

## 🚀 Features

### Zero-Dependency Setup

* Portable Python environment included
* Isolated AI engine binaries
* No registry modifications
* No package managers required
* No administrator privileges needed

### Cross-Platform Portability

Download your AI models once and use them across:

* Windows
* macOS
* Linux
* Android (Termux)

The shared storage architecture prevents duplicate model downloads, saving valuable disk space.

### Local & Private

* Completely offline operation
* No cloud services
* No internet required after setup
* All conversations remain on your device

### Network Access

The built-in web server allows access from:

* Desktop computers
* Laptops
* Smartphones
* Tablets

Simply connect devices to the same Wi-Fi network.

### Hardware Acceleration

Automatically utilizes available hardware:

| Hardware         | Support |
| ---------------- | ------- |
| AVX CPUs         | ✅       |
| NVIDIA CUDA GPUs | ✅       |
| Apple Metal GPUs | ✅       |
| Multi-core CPUs  | ✅       |

---

# 📋 System Requirements

## Storage

| Requirement | Minimum | Recommended |
| ----------- | ------- | ----------- |
| Free Space  | 8 GB    | 16 GB+      |

### Supported Media

* USB 3.0 Flash Drive
* Portable SSD
* Internal SSD
* External Hard Drive

---

## Memory Requirements

| Model Size   | Recommended RAM |
| ------------ | --------------- |
| 2B–4B Models | 8 GB            |
| 7B–9B Models | 16 GB           |
| 12B+ Models  | 24 GB+          |

---

# 📂 Folder Structure

```text
Cosmos-AI/
│
├── Android/
│   └── Android installers and launchers
│
├── Linux/
│   └── Linux installers and launchers
│
├── Mac/
│   └── macOS installers and launchers
│
├── Windows/
│   └── Windows installers and launchers
│
└── Shared/
    │
    ├── bin/
    │   └── Engine binaries
    │
    ├── chat_data/
    │   └── Conversation history
    │
    ├── models/
    │   └── AI model files
    │
    └── python/
        └── Portable Python environment
```

---

# 🤖 Included Model Recommendations

Cosmos AI supports any GGUF-compatible model.

## Lightweight Models

### Gemma 2 2B

* Extremely fast
* Low RAM usage
* Ideal for older systems
* Recommended for most users

Approximate Size: **1.6 GB**

---

## Mid-Range Models

### Gemma 4 E4B

* Better reasoning
* More detailed responses
* Excellent balance of speed and quality

Approximate Size: **5.3 GB**

---

## Advanced Models

### Qwen 3 9B

* Strong reasoning capabilities
* Higher accuracy
* Best for advanced workloads

Approximate Size: **5.2 GB**

---

## Custom Models

You may place any supported `.gguf` model directly inside:

```text
Shared/models/
```

---

# ⚡ Quick Start

## Step 1: Install Engine

Choose the installer for your operating system.

### Windows

```bat
Windows/install.bat
```

### macOS

```bash
Mac/install.command
```

### Linux

```bash
bash Linux/install.sh
```

### Android

```bash
bash Android/install.sh
```

The installer downloads the required engine binaries into:

```text
Shared/bin/
```

---

## Step 2: Download Models

Run the installer and select a model from the available catalog.

Alternatively:

1. Download a GGUF model.
2. Place it inside:

```text
Shared/models/
```

---

## Step 3: Launch Cosmos AI

### Windows

```bat
Windows/start-fast-chat.bat
```

### macOS

```bash
Mac/start.command
```

### Linux

```bash
bash Linux/start.sh
```

### Android

```bash
bash Android/start.sh
```

Your browser will automatically open the local chat interface.

---

# 💻 Local Installation

Cosmos AI can also run directly from your computer instead of a USB device.

## Installation

1. Download or clone the repository.
2. Extract it to a local drive.
3. Run the installer.
4. Download your preferred model.
5. Launch the chat interface.

### Benefits

* Faster model loading
* Better read/write performance
* Improved generation speed
* No external storage required

---

# 📱 Android Support (Termux)

Run Cosmos AI directly on Android devices.

## Requirements

* Termux (F-Droid version recommended)
* ARM64 processor
* 6 GB RAM minimum
* 8 GB+ RAM recommended

---

## Setup

```bash
bash Android/install.sh
```

Select a model and wait for installation to complete.

---

## Launch

```bash
bash Android/start.sh
```

The browser will automatically open the local interface.

---

## Android Performance Tips

* Run:

```bash
termux-wake-lock
```

* Keep Termux open while running
* Close unused applications
* Use smaller models on low-memory devices
* Connect to a charger during extended sessions

Expected performance:

| Device   | Speed             |
| -------- | ----------------- |
| 2B Model | 3–10 Tokens/sec   |
| PC + GPU | 30–50+ Tokens/sec |

---

# 🌐 Mobile Access Over Wi-Fi

Access Cosmos AI from your phone while it runs on your computer.

## Requirements

* Same Wi-Fi network
* Running Cosmos AI instance

The terminal will display an address such as:

```text
http://192.168.1.15:3333
```

Open the address in any mobile browser.

### If Access Fails

Check:

* Windows Firewall settings
* Router isolation settings
* Correct IP address

---

# 🛠 Troubleshooting

## Installer Closes Immediately

Run the installer from Command Prompt:

```cmd
install.bat
```

Or:

```cmd
Run as Administrator
```

---

## Engine Not Found

Cause:

The launcher was executed before installation.

Solution:

Run the installer first.

```bat
install.bat
```

---

## Slow Responses

Cause:

The selected model is too large for available RAM.

Solution:

Use a smaller model such as:

* Gemma 2 2B

---

## Browser Does Not Open

Open the displayed local URL manually:

```text
http://localhost:3333
```

---

# 🔒 Privacy

Cosmos AI is designed with privacy first.

* No cloud processing
* No telemetry
* No external APIs
* No account required
* All conversations remain local
