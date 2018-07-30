# Comandos necesarios para instalar las guest Additios en Debian

## Preparar nuestro S.O.

### Nos identificarnos como root
```bash
su
```

### Actualizar los repositorios del sistema operativo
```bash
apt-get update
```

### actualizar el sistema operativo
```bash
apt-get upgrade
```

### instalar el paquete build-essential
```bash
apt-get install build-essential
```
### asegurar que tengamos instaladas las cabeceras del núcleo

```bash
apt-get install linux-headers-$(uname -r) dkms
```
### instalar el paquete module-assistant 
```bash
apt-get install module-assistant
```
###  deberemos asegurar que el servidor de las X está instalado en nuestra máquina virtual

```bash
apt-get install xserver-xorg xserver-xorg-core
```
### segurar que tengamos la versión de las cabeceras del núcleo necesarias y el paquete build essential
```bash
sudo m-a prepare
```

## Instalar las Guest Additions

### Insertar Imagen CD de las Guest Additions.

### Navegar hasta la ruta de montanje

### Ejecutar el instalador 

```bash
sh ./VboxLinuxAdditions.run
```

### Reiniciar el S.O
```bash
reboot
```
