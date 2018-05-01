# Install Ansible on Windows using Cygwin

## 1. Install Cygwin
Go to https://www.cygwin.com/install.html and download `setup-x86_64.exe`
Run it
- Select 'Install from Internet'
- Choose root directory (default)
- Choose pacakage directory to store installation files
- Use System Proxy Settings
- Select any mirror site to download

### In 'Select Packages'
- select `Category` dropdown and search for `lynx`
- Go to `All -> Web -> lynx: A text-based Web Browser`
- Select latest version
- Click next to complete installation

## 2. Install `apt-cyg`
This is a package manager for cygwin

To install:
- `lynx -source rawgit.com/transcode-open/apt-cyg/master/apt-cyg > apt-cyg`
- `install apt-cyg /bin`

## 3. Install dependencies for ansible
To install altogether
- `apt-cyg install binutils curl gcc-core gmp libgmp-devel make python python-crypto python-openssl python-setuptools python-devel git nano openssh openssl openssl-devel`

You can also install individually by using
- `apt-cyg install <package_name>`
or by using the installation GUI

## 4. Install Ansible
To install
- `easy_install-2.7 pip`
- `pip install ansible -vvv`
- Here, the `-vvv` is used in case the install seems too slow. It will show you if everything is still working.

## 5. Test ansible
To test installation
- `ansible`
- Should receive list of options
