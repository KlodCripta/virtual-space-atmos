## 🛠️ SETUP GUIDE

A step-by-step guide to installing EasyEffects and loading the custom Virtual Space Atmos audio profile on Linux.

---

### ⚠️ DISCLAIMER

Virtual Space Atmos is an independent, non-commercial project and is **not affiliated with, endorsed by, or associated with Dolby Laboratories**.  
This project is entirely free and was created to partially compensate for the lack of Dolby Atmos support on Linux systems.  

Virtual Space Atmos is an **experimental audio preset** designed to enhance sound spatialization on Linux using EasyEffects.  
We take **no responsibility** for any issues, malfunctions, or damages resulting from the use of the instructions provided in this guide.  

- Some steps or behaviors may vary slightly depending on the Linux distribution, desktop environment, or system configuration.  
- Additionally, the final effect of Virtual Space Atmos may differ, either slightly or significantly, based on the audio hardware, drivers, and the headphones or speakers in use.

---

## 🎧 TESTED SETUP

### Main test machine:
- **PC:** ASUS Zenbook 14  
- **CPU:** AMD Ryzen 5  
- **Operating System:** Arch Linux KDE Plasma 6  
- **Headphones:** Sony MDR-ZX110 (On-Ear, wired; affordable but well-balanced model)  

### Secondary test machine:
- **PC:** Microtech R5  
- **CPU:** AMD Ryzen 5  
- **Operating System:** Arch Linux KDE Plasma 6  
- **Headphones:** Sony MDR-ZX110 (On-Ear, wired; affordable but well-balanced model)  

---

## 📋 REQUIREMENTS

To make Virtual Space Atmos work properly, you need the following setup:

### 1️⃣ PipeWire  
- **Required as your audio server**  
> ⚠️ This project will **not work with PulseAudio**.

### 2️⃣ EasyEffects  
- The main software used to load and manage the custom audio preset.  
- Install it from your distro’s package manager (e.g., `pacman`, `apt`, `dnf`) or via Flatpak (⚠️ *not recommended if you want system-wide integration*).

### 3️⃣ Plugins (optional but highly recommended)

Some EasyEffects modules may require additional LADSPA / LV2 plugin packages.  

**On Arch-based systems, make sure to install:**  
- `lsp-plugins`  
- `calf`  
- `zam-plugins`  
- `mda.lv2`  
- `lilv`  
- `lv2`  
- `lv2lint` (for full LV2 support)

### 4️⃣ Headphones connected  
This preset is designed and optimized exclusively for **stereo headphones**.  

Please make sure:  
- Headphones are plugged in **before launching EasyEffects**.  
- The output profile is set to **"Headphones (Stereo)"** in your audio settings.  

### 5️⃣ Enable virtual device (optional)  
If you're using multiple devices or audio interfaces (e.g., USB DACs), make sure the correct sink is selected inside EasyEffects.

---

## 📥 INSTALLATION

### Arch-based systems

EasyEffects and all required plugins can be installed from the official repositories (**not AUR**).  
Run the following command:

```bash
sudo pacman -S easyeffects lsp-plugins calf zam-plugins mda.lv2 lv2 lilv
```

> EasyEffects comes from the **extra** repo, fully official.  
> No need to enable AUR or install via Flatpak/Snap.

---

### 🛈 Note for Arch / Arch-based users with KDE Plasma  

After installing additional plugin packages (like `lsp-plugins`, `calf`, `zam-plugins`, etc.), you may notice **dozens of new icons** appear in the **Multimedia** section of your application menu (it only happened on one of the PCs used for testing).  

These are standalone plugin UIs. **You don’t need to launch them manually** to use Virtual Space Atmos with EasyEffects.

---

### Recommended solution: hide these entries from the menu  

**Quick method (KDE Plasma):**

1. Right-click on the **Start Menu** and select **Edit Applications** (This will open **KMenuEdit**).
2. Navigate to the **Multimedia** category.
3. For each unwanted item:  
   - Select it  
   - Uncheck **"Show in menus"**  
4. Save and exit  

These entries will disappear from your app menu, but all plugins will still work properly inside EasyEffects.

---

## Other Linux distributions

EasyEffects is available on most major Linux distributions, but installation methods may vary:

- **Ubuntu / Linux Mint / Debian**  
  Use `apt` or install via **Flatpak** from Flathub.  
  ⚠️ Flatpak versions are easier to install but harder to integrate system-wide.  
  *Not recommended if you want deep control or multiple profiles.*

- **Fedora**  
  Available via `dnf`, or Flathub (Flatpak).

- **Other distros**  
  Check your package manager, or install via Flatpak as fallback.  

> Plugin availability may differ. Some Flatpak versions don’t include all the needed plugins, or sandbox their functionality.

---

## ⬇️ IMPORT THE PROFILE

1. Download the latest **`VIRTUAL_SPACE_ATMOS.json`**.  
2. Open **EasyEffects**, go to **Profiles** and click **Import**.  
3. Load **`VIRTUAL_SPACE_ATMOS.json`**.  
4. Activate the preset and enjoy!

---

## 🧩 Recommended Use

- Works best with **headphones**  
- Ideal for **movies and series**, but can also enhance music  
- Can be toggled **ON/OFF** in EasyEffects during playback  

---

## 📜 License

This project is licensed under the **MIT License**.  
See the file for details.

---

## 🙌 Acknowledgements

- Developed with **EasyEffects** on Linux  
- Inspired by the need for a **free, open-source** alternative to proprietary Dolby Atmos solutions  

---

## 🤝 Contributions

Suggestions, improvements, and pull requests are welcome!  
Open an issue or contribute directly via **GitHub Issues**.
