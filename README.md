# Debian vs Arch

| Task | Debian | Arch | Notes |
| --- | --- | --- | --- |
| Update package list | sudo apt update  | sudo pacman -Sy | Refreshes repo metadata only; on Arch, pair with a full upgrade. |
| Upgrade installed packages | sudo apt upgrade | sudo pacman -Syu | Full system upgrade. |
| Install a package | sudo apt install pkg | sudo pacman -S pkg | Install from repositories. |
| Remove a package | sudo apt remove pkg | sudo pacman -R pkg | Keeps config files. |
| Remove package + deps | sudo apt purge pkg | sudo pacman -Rns pkg | Removes package, dependencies, and config files. | 
| Search packages | apt search term | pacman -Ss term | Search repositories. | 
| Show installed packages | apt list --installed | pacman -Q | List installed packages.|
| Show orphans | apt autoremove | pacman -Qdt | List orphaned dependencies; removal is often done with pacman -Rns $(pacman -Qdtq). | 
| Clean cache | sudo apt clean | sudo pacman -Sc | Remove unused cached packages. |
| Clean all cache | sudo apt autoclean | sudo pacman -Scc | Remove the whole pacman cache. |
| Check broken pkgs | dpkg --audit | pacman -Qk | Verify package files. | 

Same Commands for Both 
| Task | Debian and Arch |
| --- | --- |
| View failed services | systemctl --failed |
| View logs | journalctl -xe |
| Disk usage |  df -h | 
| Memory Usage | free -h | 
| List processes | top/htop | 
| flatpak list | flatpak list |
| flatpak update | flatpak update | 
| Symbolic Link (shortcut) | ln -s |
