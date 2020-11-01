# DOTFILES FREEBSD

Configuraciones personales en FreeBSD

BSPwm con Polybar y Rofi menu.


<img src="https://github.com/mxhectorvega/mxhectorvega.github.io/blob/master/archivos/photo_2020-10-31_21-12-07.jpg" />

<img src="https://github.com/mxhectorvega/mxhectorvega.github.io/blob/master/archivos/photo_2020-10-31_21-12-08.jpg" />

<img src="https://github.com/mxhectorvega/mxhectorvega.github.io/blob/master/archivos/photo_2020-10-31_21-15-52.jpg" />


**Crear directorios**

Crea el directorio ya que en los BSD normalmente no esta:

```
mkdir .config
```


**Configuracion**

Clonar y copiar los archivos de configuracion:

```
git clone https://github.com/mxhectorvega/dotfilesfreebsd

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




# DOTFILES ARCH LINUX
Configuraciones personales

BSPwm con Lemonbar personalizados e integrados con Dmenu y un par de scripts que facilitan el uso diario, sin sacrificar el rendimiento.

<img src="https://raw.githubusercontent.com/mxhectorvega/mxhectorvega.github.io/master/archivos/screen3.png" />

<img src="https://raw.githubusercontent.com/mxhectorvega/mxhectorvega.github.io/master/archivos/screen2.png" />

<img src="https://raw.githubusercontent.com/mxhectorvega/mxhectorvega.github.io/master/archivos/screen1.png" />

**Instalacion**

Clonar e instalar los repositorios `make && sudo make install` a travez de la terminal.

```
git clone https://github.com/baskerville/bspwm
git clone https://github.com/baskerville/sxhkd
git clone https://github.com/baskerville/xdo
git clone https://github.com/baskerville/sutils
git clone https://github.com/baskerville/xtitle
git clone https://github.com/mxhectorvega/dmenu
git clone https://github.com/mxhectorvega/tabbed
git clone https://github.com/mxhectorvega/surf
git clone https://github.com/mxhectorvega/st
git clone https://github.com/krypt-n/bar
```
**Configuracion**

Clonar y copiar los archivos de configuracion:

```
git clone https://github.com/mxhectorvega/dotfiles

cp -R ~/dotfiles/* ~/
```

Otorgar permisos de ejecucion a los archivos:

```
chmod -R +x ~/.config/{bspwm,lemonbar,ranger}
```

En caso de no tener pantalla de inicio de sesion, agregar `exec bspwm` al
archivo **~/.xinitrc, .xprofile o start.sh** (si no cuenta con el archivo, cree uno nuevo y asigne
permisos de ejecucion con `chmod +x`).

**Dependencias**

```
sudo pacman -S gvfs devmon devilspie xcompmgr ueberzug youtube-dl ffmpegthumbnailer gst-plugins-good gst-libav feh mpd mpc ncmpcpp slock firefox telegram-desktop htop xarchiver neofetch leafpad ranger pcmanfm lxappearance dunst maim xclip sxiv xdotool calcurse zathura zathura-pdf-mupdf neovim mpv screenkey

yay -S transset-df

```

**Fuentes y temas**

```
yay -S otf-sfmono nerd-fonts-mononoki ttf-joypixel sotf-font-awesome-5-free awesome-terminal-fonts ttf-menlo-powerline-git otf-san-francisco-compact nerd-fonts-sf-mono materia-gtk-theme materia-kde papirus-icon-theme
```

**Bordes de ventanas redondeados (opcional)**

```
picom-ibhagwan-git
```

**Drives de Pulseaudio (opcional)**

```
sudo pacman -S pulseaudio pulseaudio-alsa pulseaudio-bluetooth alsa-utils alsa-plugins
```

**Software de uso personal (opcional)**

```
sudo pacman -S libreoffice-fresh-es kdenlive audacity gimp inkscape

yay -S spotify spotify-adblock-linux --noeditmenu --noconfirm --needed
```

**Grupo telegram:**

https://t.me/wmesp

**Canal de tips:**

https://t.me/mxhectorvega

**Creditos:**

@mxhectorvega @tenshalito @bourne_again @darch7 @codeassault
