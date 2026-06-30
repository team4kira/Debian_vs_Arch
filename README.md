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
| Task | Debian | Arch | Notes |
| --- | --- | --- | --- |
| Update package list | sudo apt update  | sudo pacman -Sy | Refreshes repo metadata only; on Arch, pair with a full upgrade. |
| 02 | XSS Stored | Medium |
| 03 | Local File Injection | High |
| 04 | SQL Injection | Critical |
| 05 | Weak Password on Web Application | Critical |
| 06 | Command Injection | Medium |
| 07 | PHP Injection | Critical |
| 08 | Brute Force Attack | Medium |
| 09 | Directory Traversal | Medium |
| 10 | Apache Tomcat Remote Code Execution Vulnerability | High |
| 11 | Shellshock | Critical |
| 12 | Struts | High |
| 13 | Drupal | High |
| 14 | Password Guessing in SSH | Critical |
| 15 | Sudo Command Privilege Vulnerability | Critical |
| 16 | FTP Anonymous Vulnerability | High |
| 17 | Slmail Vulnerability | Critical |
| 18 | LSAdump Attack | High |
| 19 | WMI Vulnerability | Critical |
| 20 | DCSync Attack | Critical |
