# Arch Linux Install
Preperation:
Navigate to archlinux.org/download and download a arch iso from your region

Aquire and launch VM application of your choice

Create new VM using the arch linux iso obtained earlier

.

Installation:
Once the VM has loaded, type archinstall in the terminal line

This will take you to an installation menu

Select desired language, region for mirrors, specification for locales, and boot loader (grub recommended)

Use default partitions with the btrfs layout

Feel free to change the hostname to anything desired, I will be using archvm for simplicity

Input a secure and safe password for the root password

Create 3 users (project specific), yourself, justin, and codi

justin and codi should have the password "GraceHopper1906" and codi should be given sudo privileges

Continue with the installation by selecting install and wait as arch configures and installs

Select yes to continue into the new installaiton with chroot

.

Desktop Enviroment:

Type pacman -S gnome (I will be using gnome for the desktop enviroment)

Press enter when prompted to fully install gnome

Select whichever option for the following emoji and jack choices

After Gnome is fully downloaded, we will restart the vm in order to boot into the gui

Type "exit" to leave chroot and then "shutdown now" in the cli to shutdown the vm

Navigate to the settings portion of the vm software being used and in the System tab, uncheck the optical disk in order to not boot a new installation instance

After the vm turns on again and you have logged in with your credentials, the gnome display manager must be enabled, to do this type systemctl enable gdm.service after switching to the root user in order to run as sudo

Launch gnome by running systemctl start gdm.service and patiently waiting for the desktop enviroment to start

.

ZSH:

In the terminal, type pacman -S zsh zsh-completions while in root to run as sudo

Run zsh by typing zhs and responding 0

Set zsh to the default shell by entering the command chsh -s /usr/bin/zsh 

.

Theme:

To install a new theme for zsh I will be using an Oh My Zsh distribution

Install by running sh -c “$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)”

.

Aliases:

Access the file zshrc by running nano .zshrc

Write whatever aliases you wish using the format aliase=command
