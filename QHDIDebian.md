# ¿Que hacer despues de instalar Debian 9 stretch?

## Configuración e instalación de software

1. Modificamos los repositorios oficiales
* Nos identificarnos como root
```bash
    su
```
* actualizamos la lista de paquetes 
```bash
    apt-get update
```
* actualiazamos el S.O
```bash
    apt-get upgrade
```
* accedemos a los repositorios

```bash 
    $ nano /etc/apt/sources.list
```
* editamos el fichero sources.list
```bash
    # 

    # deb cdrom:[Debian GNU/Linux 9.5.0 _Stretch_ - Official amd64 NETINST 20180714-10:25]/ stretch main

    #deb cdrom:[Debian GNU/Linux 9.5.0 _Stretch_ - Official amd64 NETINST 20180714-10:25]/ stretch main

    deb http://ftp.es.debian.org/debian/ stretch main contrib non-free
    deb-src http://ftp.es.debian.org/debian/ stretch main contrib non-free

    deb http://security.debian.org/debian-security stretch/updates main contrib non-free
    deb-src http://security.debian.org/debian-security stretch/updates main contrib non-free

    # stretch-updates, previously known as 'volatile'
    deb http://ftp.es.debian.org/debian/ stretch-updates main contrib non-free
    deb-src http://ftp.es.debian.org/debian/ stretch-updates main contrib non-free
```
* actualizamos la lista de paquetes 
```bash
    apt-get update
```
* actualizamos el S.O
```bash
    apt-get upgrade
```

2. Instalación del gestor gráfico de paquetes Synaptic

* Nos identificarnos como root
```bash
    su
```
* actualizamos la lista de paquetes 
```bash
    apt-get update
```
* actualizamos el S.O
```bash
    apt-get upgrade
```
* instalamos synaptic
```bash
    apt-get install synaptic
```
* activamos el filtro rápido
```bash
    apt-get install apt-xapian-index
```
3. Software del sistema
* Cabeceras y constructores
```bash
    apt-get install linux-headers-$(uname -r)
    apt-get install build-essential checkinstall make automake cmake autoconf git git-core dpkg wget
```
* instalador gráfico de .deb
```bash
    apt-get install gdebi
```
* instalador gráfico de .deb (kde)
```bash
    apt-get install gdebi-kde
```
4. controladores gráficos
```bash
    apt-get install firmware-linux
```
5. codecs multimedia (no oficial)

* accedemos a los repositorios

```bash 
    $ nano /etc/apt/sources.list
```
* editamos el fichero sources.list
```bash
    # Multimedia
    deb http://www.deb-multimedia.org/ stretch main contrib non-free

```
* descargamos el keyring desde deb-multimedia.org
```bash
    wget http://deb-multimedia.org/pool/main/d/deb-multimedia-keyring/deb-multimedia-keyring_2016.8.1_all.deb
```
* Instalamos el keyring
```bash
    dpkg -i deb-multimedia-keyring_2016.8.1_all.deb
```
* actualizamos la lista de paquetes 
```bash
    apt-get update
```
* actualizamos el S.O
```bash
    apt-get upgrade
```
* instalamos codecs reproducción de CDs
```bash
    apt-get install libdvd-pkg
```
6. Tipografías
* tipografías libres
```bash
    apt-get install fonts-freefont-ttf fonts-freefont-otf
```
* tipografías de microsoft
```bash
    apt-get install ttf-mscorefonts-installer
```
7. Java
* OpenJDK
```bash
    apt install openjdk-8-jre icedtea-8-plugin
```
8. Herramientas de compresión y descompresión
* rar, zip, 7zip y alguno más
```bash
    apt-get install rar unrar zip unzip unace bzip2 lzop p7zip p7zip-full p7zip-rar
```
9. Gestión de discos y particiones
* instalar disk manager
```bash
    apt-get install disk-manager
```
10. Instalar Google Chrome
* Agregamos los repositorios 
```bash
   echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" > /etc/apt/sources.list.d/google-chrome.list
```
* Agregamos el keyring (llaves) para google
```bash
  wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add -
```
* actualizamos la lista de paquetes 
```bash
    apt-get update
```
* instalamos google chrome
```bash
    apt-get install google-chrome-stable
```
