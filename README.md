# Debian_vs_Arch
Common commands found in Debian and Arch
**Task	Debian	Arch	Notes
Update package list	sudo apt update	sudo pacman -Sy	Refreshes repo metadata only; on Arch, pair with a full upgrade. 
Upgrade installed packages	sudo apt upgrade	sudo pacman -Syu	Full system upgrade.
Install a package	sudo apt install pkg	sudo pacman -S pkg	Install from repositories. 
Remove a package	sudo apt remove pkg	sudo pacman -R pkg	Keeps config files. 
Remove package + deps	sudo apt purge pkg	sudo pacman -Rns pkg	Removes package, dependencies, and config files. 
Search packages	apt search term	pacman -Ss term	Search repositories. 
Show installed packages	apt list --installed	pacman -Q	List installed packages. 
Show orphans	apt autoremove	pacman -Qdt	List orphaned dependencies; removal is often done with pacman -Rns $(pacman -Qdtq). 
Clean cache	sudo apt clean	sudo pacman -Sc	Remove unused cached packages. 
Clean all cache	sudo apt autoclean	sudo pacman -Scc	Remove the whole pacman cache. 
Check broken pkgs	dpkg --audit	pacman -Qk	Verify package files.
View failed services	systemctl --failed	systemctl --failed	Same command on both.
View logs	journalctl -xe	journalctl -xe	Same command on both. 
Disk usage	df -h	df -h	Same command on both. 
Memory usage	free -h	free -h	Same command on both. 
List processes	top / htop	top / htop	Same command on both. 
Update whole system incl. AUR	n/a	yay -Syu	Common on Arch if you use an AUR helper. reddit+1
Search AUR package	n/a	yay -Ss term	AUR helper command. 
**
