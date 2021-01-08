# INSTALLARCH
<img src="https://raw.githubusercontent.com/mxhectorvega/installarch/master/installer2.png" />
**SCRIPT DE INSTALACIÓN EXPRESS ARCHLINUX SIN ENTORNO GRÁFICO**


**La instalacion contiene:**
Drivers wifi, bluetooth, video, audio y servidor X (xorg).


**Instrucciones:**
1. Iniciar en modo uefi o bios con el LiveUSB de ArchLinux
2. ``loadkeys es`` (o segun la distribucion del teclado ``la-latin1, es, en``)
3. ``curl https://mxhectorvega.github.io/installarch > installarch ; sh installarch``
4. Seleccionar la unidad conectada donde se instalara ejemplo: ``/dev/sdx``:
5. Ingrese una contraseña root:
6. Ingrese un nombre de usuario estándar:
7. Ingrese una contraseńa para el usuario estándar :
8. Ingrese un nombre para el equipo:
9. Ingrese localizacion del idioma ejemplo ``es_MX.UTF-8`` o ``es_AR.UTF-8``


**Canal youtube:**
https://youtube.com/mxhectorvega
**Canal telegran:**
https://t.me/mxhectorvega


**Creditos:**
@mxhectorvega @darch7 @cristoalv @bourne_again






-






# DOTFILES ARCH LINUX
Configuraciones personales

BSPwm, polybar, rofi y un par de scripts que facilitan el uso diario, sin sacrificar el rendimiento.

<img src="https://raw.githubusercontent.com/mxhectorvega/dotfilesarchlinux/main/screenshot.png" />


**Importante:**

Puede probar esta configuracion en una Maquina Virtual QEMU, VirtualBox, etc., instalando con mi script de instalacion rapida de ArchLinux, donde solo instala lo basico hasta el servidor X y asi probar sin afectar a su SO ppal.
https://raw.githubusercontent.com/mxhectorvega/installarch/main/qemuxorg

**Instalacion**

Instalar BSPwm, Sxhkd y Rofi (para que funcione rofi con los temas debe instalar pywal desde pip3 `pip install pywal`).

```
sudo pacman -S bspwm sxhkd rofi
```

Instalar polybar.

```
yay -S polybar-git
```

Clonar e instalar el repositorio `make && sudo make install` a travez de la terminal.

```
git clone https://github.com/mxhectorvega/st
```

**Configuracion**

Clonar y copiar los archivos de configuracion:

```
git clone https://github.com/mxhectorvega/dotfilesarchlinux

mkdir .local
mkdir .local/share

cp -R ~/dotfilesarchlinux/.config/* ~/.config
cp -R ~/dotfilesarchlinux/.local/* ~/.local

chmod + x ~/.config/bspwm/*
chmod + x ~/.local/bin*
```

En caso de no tener pantalla de inicio de sesion, agregar en la linea 1: `sxhkd &` y en la linea 2: `exec bspwm` al
archivo **~/.xinitrc, .xprofile o zprofile** (si no cuenta con el archivo, cree uno nuevo y asigne
permisos de ejecucion con `chmod +x`).

**Dependencias**

```
sudo pacman -S bc tmux imagemagick ueberzug ffmpegthumbnailer feh mpd mpc ncmpcpp slock telegram-desktop htop xarchiver neofetch leafpad ranger pcmanfm lxappearance dunst maim xclip sxiv xdotool calcurse zathura zathura-pdf-mupdf neovim mpv screenkey --noconfirm --needed
```

**Temas**

```
sudo pacman -S materia-gtk-theme materia-kde papirus-icon-theme --noconfirm --needed
```

**Bordes de ventanas redondeados (opcional)**

```
yay -S picom-ibhagwan-git --noconfirm --needed
```

**Cosas que se ven en la terminal**

```
yay -S cava-git cmatrix unimatrix pfetch tty-clock --noconfirm --needed
```

**Software de uso personal (opcional)**

```
sudo pacman -S geany python-pip obs-studio libreoffice-fresh-es kdenlive audacity gimp inkscape --noconfirm --needed

yay -S spotify spotify-adblock-linux --noeditmenu --noconfirm --needed
```

**En caso de no tener instalado YAY:**

```
git clone https://aur.archlinux.org/yay.git ; cd yay ; makepkg -si ; cd ~ ; rm -rf yay
```

**NOTA:**
Los scripts esta en el directorio `.local/bin` donde podra modificarlos o tomar parte del codigo.

**NOTA:**
Para agregar o quitar modulos de polybar, debera modificar la linea 47 de `.config/polybar/config` segun el nombre asignado ejemplo [module/fecha] el modulo es: fecha


**Grupo telegram:**
https://t.me/wmesp


**Canal de tips:**
https://t.me/mxhectorvega


**Creditos:**
@mxhectorvega @tenshalito @bourne_again @darch7 @codeassault






-






# DOTFILES FEDORA

Configuraciones personales en Fedora 33

BSPwm con Polybar y Rofi menu.


<img src="https://raw.githubusercontent.com/mxhectorvega/dotfilesfedora/main/screenshot.png" />


**Configuracion**

Clonar y copiar los archivos de configuracion:

```
git clone https://github.com/mxhectorvega/dotfilesfedora

cp -R ~/dotfiles/.config/* ~/.config

cp ~/dotfiles/.config/.Xresources ~/.Xresources
```


Crear el archivo `.xinitrc` y agregarle la linea `exec bspwm`:

```
vim .xinitrc
```


Otorgar permisos de ejecucion a los archivos:

```
chmod +x .config/bspwm/bspwmrc

chmod +x .xinitrc
```


**Dependencias**

```
sudo dnf install xterm bspwm sxhkd mpd mpc ranger nvim pcmanfm feh pip37 python37 mntui intel_xbacklight 

pip install pywal
```

**Temas**

```
sudo dnf install papirus-icon-theme materia-gtk-theme
```


**Grupo telegram:**

https://t.me/fedoralinuxes

**Canal de tips:**

https://t.me/fedora_tips

**Creditos:**

@mxhectorvega @DonatelloSanz 






-






# DOTFILES FREEBSD

Configuraciones personales en FreeBSD

BSPwm con Polybar y Rofi menu.


<img src="https://raw.githubusercontent.com/mxhectorvega/mxhectorvega.github.io/master/archivos/photo_2020-10-31_21-12-07.jpg" />


**Crear directorios**

Crea el directorio ya que en los BSD normalmente no esta:

```
mkdir .config
```


**Configuracion**

Clonar y copiar los archivos de configuracion:

```
git clone https://github.com/mxhectorvega/dotfilesfreebsd

cp -R ~/dotfilesfreebsd/.config/* ~/.config

cp ~/dotfilesfreebsd/.Xresources ~/.Xresources
```


Crear el archivo `.xinitrc` y agregarle la linea `exec bspwm`:

```
vim .xinitrc
```


Otorgar permisos de ejecucion a los archivos:

```
chmod +x .config/bspwm/bspwmrc
chmod +x .xinitrc
```


**Dependencias**

```
pkg install py37-pip python37 ncpamixer ImageMagick7 py27-ranger picom youtube_dl feh sxiv musicpd musicpc ncmpcpp firefox telegram-desktop htop xarchiver neofetch leafpad pcmanfm lxappearane zathura zathura-pdf-mupdf neovim mpv

pip install pywal
```

**Temas**

```
pkg install papirus-icon-theme materia-gtk-theme
```


**Grupo telegram:**

https://t.me/bsdesp

**Canal de tips:**

https://t.me/bsd_tips

**Creditos:**

@mxhectorvega @DtxdF @ozunalexis @AlexHMusique @Lunatic_101
