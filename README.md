---

<h1 align="center">TensorFlow in Android (ARM64) via Termux + Pyenv</h1>

<p align="center">
  <b>Run TensorFlow 2.13.1 (CPU) natively on Android ARM64 using Termux and Pyenv</b><br><br>
  <img src="https://img.shields.io/badge/Platform-Android%20ARM64-blue.svg" />
  <img src="https://img.shields.io/badge/TensorFlow-2.13.1-orange.svg" />
  <img src="https://img.shields.io/badge/Python-3.8.18-green.svg" />
  <img src="https://img.shields.io/badge/Shell-Termux-informational.svg" />
</p>

---

## Overview

This guide walks you through setting up **TensorFlow 2.13.1** (CPU version) on **Android devices** running **Termux** and **Pyenv**, enabling you to run machine learning models and leverage TensorFlow's full capabilities — all without needing root access.

This setup is **unique** and **cutting-edge** for ARM64 Android devices. Most setups don’t enable TensorFlow directly in Termux, but here’s how you can do it, making it a **powerful tool** for those looking to experiment with AI on mobile devices.

---
<p align="center">
  <img src="banner.png" alt="TensorFlow in Android by mikey-7x" width="800"/>
</p>

---

## Requirements

### Supported Platforms:

- **Android ARM64** (any recent Android device with ARM64 architecture)
- **Termux**: a Linux environment on Android
- **Pyenv** and **Python 3.8.18**
- **TensorFlow 2.13.1** (latest working version for ARM64)

---

## Installation Instructions

1. Install Required Dependencies

First, choose the appropriate package manager based on your platform.

**For Ubuntu/Debian-based systems (APT):**

```bash
sudo apt update && sudo apt install -y \
    git curl gcc make zlib1g-dev libssl-dev libffi-dev build-essential
```

**For Arch Linux-based systems (PACMAN):**

```
sudo pacman -S --noconfirm \
    git curl gcc make zlib openssl libffi

```
---

2. Install Pyenv and Pyenv-Virtualenv

Run the following to install pyenv:
```
curl https://pyenv.run | bash
```

After installation, update your shell configuration file (~/.bashrc or ~/.zshrc), and add the following lines at the bottom:
```
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv virtualenv-init -)"
```

Once you've added the lines, apply changes:
```
source ~/.bashrc  # or source ~/.zshrc for Zsh
```

---

3. Install Python 3.8.18
```
Install the correct version of Python:
```

pyenv install 3.8.18


---

4. Create and Activate Virtual Environment for TensorFlow

Now, create a dedicated virtual environment for TensorFlow:
```
pyenv virtualenv 3.8.18 tf-env
pyenv activate tf-env
```

To verify Python version:
```
python --version
```

Expected output: Python 3.8.18


---

5. Install TensorFlow

Now, you can install TensorFlow with a simple pip command:
```
pip install tensorflow
```

---

6. Verify TensorFlow Installation

To ensure everything is working correctly, check TensorFlow's version:
```
python -c "import tensorflow as tf; print(tf.__version__)"
```

Expected output: 2.13.1


---

**Quick Reference**

Command	Description

pyenv versions	List installed Python versions
pyenv activate tf-env	Activate TensorFlow virtual environment
pyenv deactivate	Deactivate the environment
pyenv uninstall tf-env	Uninstall the virtual environment
pip list	List all installed Python packages



---

**Environment Details**

Device: Android ARM64

Termux OS: Arch Linux / Ubuntu (via proot)

Python Version: 3.8.18

TensorFlow Version: 2.13.1 (CPU)


---


**Conclusion**

By following this guide, you’ve successfully set up TensorFlow 2.13.1 on your Android ARM64 device using Termux and Pyenv, without needing root access. This is a cutting-edge, professional setup for anyone working on mobile AI or machine learning projects.


---

# 🍁Contribution

If you found this setup useful, feel free to fork, contribute, or improve this repository by submitting a pull request.


---

# 🪽Special Thanks

TensorFlow ARM64 Builds

Pyenv

Termux Project

---

# 📜License

This project is open-source and available under the [MIT License](LICENSE).

---

# ☕Credits

Developed with  ❤️ by **[mikey-7x](https://github.com/mikey-7x)** 🚀🔥  

> Made with passion and precision — by [mikey-7x]



---

