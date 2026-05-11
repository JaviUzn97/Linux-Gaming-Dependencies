This script is a comprehensive **Post-Installation & Dependency Setup** tool designed to prepare various Linux distributions for gaming, multimedia, and general productivity. It automates the installation of essential graphics drivers (Vulkan/Mesa), multimedia codecs, and system dependencies, while also ensuring Microsoft-compatible fonts are available for document compatibility.

---

# Linux Gaming & Multimedia Setup Script

A lightweight bash script to automate the installation of essential drivers, codecs, and dependencies across multiple Linux distributions. This is ideal for fresh installations or for users setting up their systems for gaming (Steam, Wine, RetroArch) and media playback.

## 🚀 Features

* **Multi-Distro Support:** Automatically detects and configures Debian, Ubuntu, Kubuntu, Arch Linux, Fedora, openSUSE, and Solus.
* **Graphics & Vulkan:** Installs 32-bit and 64-bit Vulkan loaders and Mesa drivers, critical for modern gaming and performance.
* **Multimedia Codecs:** Sets up GStreamer plugins (Base, Good, Bad, Ugly, and Libav) for seamless video and audio playback.
* **Microsoft Fonts:** Clones and installs Microsoft 365 fonts to ensure document compatibility and better web rendering.
* **Architecture Setup:** Automatically enables `i386` architecture on Debian-based systems to support legacy applications and gaming.

---

## 🛠️ Requirements

* A supported Linux distribution (Debian, Ubuntu, Kubuntu, Arch, Fedora, openSUSE, or Solus).
* `sudo` privileges to install system packages.
* An active internet connection.

---

## 📂 Installation & Usage

1. **Clone the repository or download the script:**
```bash
git clone https://github.com/your-username/your-repo-name.git](https://github.com/JaviUzn97/Linux-Gaming-Dependencies.git
cd Linux-Gaming-Dependencies

```


2. **Make the script executable:**
```bash
chmod +x gaming-dependencies

```


3. **Run the script:**
```bash
./gaming-dependencies

```



---

## 📝 What the Script Does (By Category)

### 1. Distribution Detection

The script reads `/etc/os-release` to identify your operating system and executes the specific package manager commands (`apt`, `pacman`, `dnf`, `zypper`, or `eopkg`) required for your environment.

### 2. Graphics Drivers (Vulkan/Mesa)

It installs the necessary libraries to enable hardware acceleration. This includes `libvulkan`, `mesa-vulkan-drivers`, and `intel-media-va-driver`, ensuring both Intel and AMD/generic graphics work optimally.

### 3. Multimedia Support

It installs the "Ugly" and "Bad" GStreamer plugins, which contain restricted but necessary codecs for playing various proprietary video and audio formats.

### 4. Font Integration

The script creates a local font directory (`~/.local/share/fonts`), clones a repository of Microsoft 365 fonts, and updates the system font cache (`fc-cache`) so they appear immediately in your applications.

---

## ⚠️ Important Notes

* **Arch Linux Users:** Ensure the `[multilib]` repository is enabled in your `/etc/pacman.conf` before running the script to allow 32-bit library installation.
* **NVIDIA Users:** While this script installs Vulkan loaders and Mesa tools, you should still ensure your proprietary NVIDIA drivers are installed via your distribution's driver manager for the best experience.

---

## 🤝 Contributing

Feel free to fork this project, report issues, or submit pull requests to add support for more distributions or additional essential tools.
