# gruvbox-dotfiles
# Welcome to my dotfiles! First you have to install this stuff:
sudo pacman -S bspwm sxhkd polybar picom rofi dunst nitrogen alacritty thunar base base-devel git i3lock-color neofetch neovim cava feh curl zsh lxappearance kvantum-qt5

sudo pacman --sync flameshot

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

git clone https://github.com/Fausto-Korpsvart/Gruvbox-GTK-Theme.git

# now you have to setup bspwm if it's your first time using it:
cd $HOME/.config

mkdir bspwm sxhkd polybar picom dunst

cp /usr/share/doc/bspwm/examples/bspwmrc bspwm/

cp /usr/share/doc/bspwm/examples/sxhkdrc sxhkd/

cp /etc/xdg/picom.conf picom/

cp /etc/polybar/config.ini polybar/

cp /etc/dunst/dunstrc dunst/

chmod +x bspwm/bspwmrc

# install yay
git clone https://aur.archlinux.org/yay.git 

cd yay && makepkg -si

# install gruvbox theme
yay -S gruvbox-dark-gtk

sudo mv Gruvbox-GTK-Theme /usr/share/themes/

# optional stuff

sudo pacman -S flatpak vlc signal-desktop telegram-desktop spotify-launcher gparted firefox libreoffice-fresh ufw thunderbird
sudo systemctl enable bluetooth

