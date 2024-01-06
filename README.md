# Python Versioned Environments

This repository demonstrates how to create and manage different Python virtual environments for various Python versions using `python3-venv`.

## Introduction

When working on projects that require specific Python versions or need isolation from system-wide Python packages, creating virtual environments is a good practice. This repository provides a guide on how to set up virtual environments for different Python versions.

## Instructions

### 1. Install Python from the Official Website (Optional)

If you prefer to download and compile Python directly from the official Python website, follow these steps:

#### 1.1 Install necessary build dependencies:

```bash
sudo apt-get update
sudo apt-get install -y build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev libsqlite3-dev wget libbz2-dev
```

#### 1.2 Download and compile Python:

Replace X.Y.Z with the version number you want to install (e.g., 3.8.12):

```bash
wget https://www.python.org/ftp/python/X.Y.Z/Python-X.Y.Z.tgz
tar -xf Python-X.Y.Z.tgz
cd Python-X.Y.Z
./configure --enable-optimizations
make -j$(nproc)
sudo make altinstall
```

#### 1.3 Verify installation:

Check the installed Python version:

```bash
python3.8 -V
```

### 2. Create Virtual Environments Using `python3-venv`

#### For Python 3.8:

```bash
python3.8 -m venv venv38
```

Activate the virtual environment:

```bash
source venv38/bin/activate
```

#### For Python 3.9:

```bash
python3.9 -m venv venv39
```

Activate the virtual environment:

```bash
source venv39/bin/activate
```

### 3. Install `virtualenv` (Optional)

```bash
pip install virtualenv
```

### 4. Use the Virtual Environments

Within each activated virtual environment, use `pip` to install project-specific dependencies:

```bash
pip install package_name
```

### 5. Deactivate the Virtual Environments

When you're done working in a virtual environment, deactivate it:

```bash
deactivate
```

### 6. Delete Virtual Environments (Optional)

To delete a virtual environment, run:

```bash
rm -rf path/to/venv
```

### 7. Contributing

Feel free to contribute improvements, additional instructions, or support for other Python versions!

