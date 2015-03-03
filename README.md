### [download built images at SourceForge](https://sourceforge.net/p/hackeurs-sans-frontieres), forums are there too  
![LXQt desktop](https://sourceforge.net/p/hackeurs-sans-frontieres/screenshot/screenshot_4.png)  

This is hybrid live cd/usb openSUSE spin aimed to be fully functional out-of-the-box yet slim desktop system for hackers of all sorts: technical, humanitarian, artistic, social and so on.  
It DOES NOT guarantee best security defaults, so users with sensitive needs are advised to direct their attention to something like [TAILS](https://tails.boum.org), [CAINE](https://www.caine-live.net) or [Whonix](https://www.whonix.org), however it should be quite adequate as an installation basis for everyday use and comes with pre-configured data proxying via [Tor](https://www.torproject.org/about/overview.html) & [DNSCrypt](http://dnscrypt.org).

I recommend using smart SATA boxes and usb drives with legacy (floppy / CD / virtual partition) emulation as the replacement for disks, like:  
⊘ [IODD](https://iodd.co.kr) / [Zalman ZM-\*](https://www.zalman.com/global/product/CategorySecond_Pic.php) series  
⊘ [The IsoStick](https://isostick.com)  
⊘ or just using it on any fast USB stick  

It provides:
------------
* complete toolkit that created it
* fresh stable kernel from Kernel:stable repo
* fresh (enabled) OSS video stack from X11 repo (rc's)  
or bleeding edge (configured) from pontostroy (git & kernel rc's)
* LXQt slim desktop environment
* international collection of fonts and universal iBus input method by default
* LibreOffice, GIMP and fresh GoldenDict;  
Calibre, okular, kchmviewer, djvulibre-djview4 and pdfcrack
* codecs, font antialiasing and texture compression support  
without artificial restrictions
* bomi/mpv (ex-C/Mplayer) video and Tano IPTV players, VLC Firefox plugin;  
SubtitleComposer and Aegisub subtitle editors, Trackma anime/manga tracker
* professional sound handling with JACK  
(PA & ALSA, both with OSS emulation, run as JACK's clients)
* Clementine audio player, Audacity audio editor/recorder;  
GStreamer with FFMPEG and JACK output by default
* professional colour management facilities  
(consisting of colord, argyllCMS, dispcalGUI and xiccd)
* printer (via cups), scanner (via x/sane)  
and analogue video input (via tvtime) support
* professional screencasting tool SimpleScreenRecorder with native JACK support
* wide range of gamepad utilities  
such as AntiMicro (for key & axis mapping) and jstest-gtk
* professional virtualization with libvirt & KVM / LXC  
(featuring userland virt-manager and SPICE flowing out-of-the-box)
* professional networking tools and rich connectivity options
* OpenVAS and ClamAV security systems
* anti-censorship kit: Tor/Polipo, dnscrypt-proxy/Unbound, proxychains and VPN
* LeechCraft modular system stripped for only IM and socializing
* LinPhone & SIP Witch for P2P HD A/V multiuser {S/Z}RTP-encrypted telephony;  
Tox network clients for Tor/BitTorrent-like P2P A/V telephony (or so they say)
* fresh Mozilla Firefox browser and Thunderbird e-mail client
* qBitTorrent, aMule, Filezilla & lftp, wget & aria2/fe and httrack for file transfer
* mc, zsh, kmscon, android-tools, wgetpaste/pastebinit and other console tools
* networking tools:  
  * interconnecting: hostapd, usbip, miredo-client, minicom and rancid
  * looking: {arp-,ike-,ssl}scan, iptraf-ng, nethogs, upnp-inspector, mtr{-gtk}, lft
  * touching: wireshark-qt, {ze}nmap, wapiti, xprobe2, scapy & nping, aircrack-ng, kismet, reaver
  * filesharing: nfs-kernel-server, pure-ftpd, samba
* filesystem tools:  
  * management: gparted, {f/g}disk, gptfdisk-fixparts, guestfs-tools, snapper, disktype, exfat kernel module
  * recovery/imaging: fsarchiver{-qt4}, guymager, xmount, ddrescue, testdisk, photorec, foremost, ext4magic
  * support for pretty much all filesystems known to man, in kernel or via FUSE
* security/forensics tools:  
  * autopsy/sleuthkit, scalpel, [plaso/log2timeline](http://plaso.kiddaland.net) & [Windows®-gutting toolkit](https://github.com/libyal), chkrootkit/rkhunter, ntpassw/dchntpw/ophcrack, lynis
* encryption tools:  
  * tc-play (TrueCrypt reimplementation), aespipe, emount/zuluCrypt/cryptsetup, seahorse/gnome-keyring, keepassx
* useful things that I've put there but forgot to mention
* bunch of repos pre-configured (but disabled) for games, emulators  
and recent though mostly stable updates

It does NOT provide:
--------------------
— Windows® compatibility, wine (because it requires shitload of 32bit packages)  
— proprietary video drivers (because they suck and are pain in the ass).  
  or video driver support for anything without KMS, for that matter  
— whole KDE or Gnome (because of how fat the former and how ugly the later are)  
— any language translation packages (for space conservation)  
— Wayland packages (because it's too raw yet)  
— many cd/dvd/bluray and whatever disk tools (because spinning media must die).  
  cdrkit-cdrtools-compat and cdemu are included though  
— accessibility features (because I have no idea how to setup them right)  
  but there is `onboard` virtual keyboard  
— security hardening (because it requires strict and thorough testing  
  in all usage scenarios which are manifold)  

Notes:
------
⊙  **the first thing you should do on freshly loaded system is to look at gnote's HSF note**  
⊙ use `locate` to search for files fast and `apropos` to search for commands based on their manual's description  
⊙ Firefox and Thunderbird are set up to use Tor by default, *_proxy variables are also globally set, DNS queries are encrypted and funneled to OpenDNS by default  
⊙ popular Microsoft fonts are included for web & document compatibility. they may be removed in future  

⊙ can be put on flash USB sticks and such from within itself by  
* simple `dd bs=<your flash's write block size, like 64K> if=<image or even cdrom device that you have booted it on> of=/dev/<target_device>`
* or glamorous GUI tool like `unetbootin` (included), SUSE's `imagewriter` or Ubuntu's `win32diskimager`

⊙ DE-specific apps are included for the lack of adequate analogues  
* KDE:  
  * krusader (dolphin + konqueror + mc in one package and more ? yes, please)  
  * yakuake (handy console), will be replaced with finalterm once it matures  
  * kate/kwrite (great simple editor)  
  * okular (useful doc viewer, integrated in Firefox via kparts-plugin)  
  * kchmviewer (MS chm viewer), because sometimes okular screws up  
  * gwenview + kipi-plugins (highly-capable image viewer)  
* GNOME:  
  * nm-applet (this is _the only_ NM GUI that can launch in any DE)  
  * blueman (bluez5 control)  
  * gparted (The F/OSS disk editor), even though it can be substituted with YaST  
  * pasystray (PulseAudio control) and all its dependencies  
  * easytag (The audio file tag editor)  
  * seahorse (gpg GUI)  
  * gcr-viewer (crypto file viewer)  

⊙ Some specialty apps that were not included but you may be interested in installing manually  
* music works  
  * ardour3, rosegarden, qtractor, hydrogen, mixxx, rakarrack, OpenOctaveMidi, vmpk  
* high-quality midi playback  
  * fluid-soundfont-gs, fluidsynth, qsynth, kmid  
* video editing  
  * cinelerra, LiVES, openshot, avidemux, kino  
* 3D modeling  
  * blender  
* design  
  * OpenCASCADE, FreeCAD, librecad, qcad, openscad, kicad, QCADesigner  
* publishing  
  * scribus  
* office works utilities  
  * chm2pdf  
  * djvu2pdf/pdf2djvu  
* painting  
  * cinepaint, mtpaint  
* vector drawing  
  * inkscape, sk1  
* vector drawing utilities  
  * autotrace, uniconvertor/uniconvw  
* font creation  
  * fontforge  
* OCR (image_of_text-to-real_text conversion)  
  * yagf (xsane OCR wrapper)  
  * djvubind or ocrodjvu/img2djvu (DjVu-centric wrappers for OCR systems)  
  * tesseract-{gui} / cuneiform / gocr{-gui} / orcad / ocropus (OCR systems)  
* telephony  
  * sflphone-client-gnome (SIP client that natively supports JACK and has many features... and glitches)  
  * blink (supposedly is "the best real-time communications client using SIP protocol". ALSA-only and crash-prone)  
  * ekiga (simple but ALSA-only)  
  * yate-qt4 (lots of features with no GUI for them)  
  * jitsi (Jack-of-all-trades and JAVA-fatass)  
* multimedia  
  * SMplayer GUI for mpv & mplayer (allows extreme fine-tuning but is full of legacy code)  
  * VLC (the king of media players but it's interface sucks)  
  * QMPlay2 (vlc-like player with better GUI but without JACK support)  

Building:
---------
* ∀ every build comes with its building source in '/home/hacker/Hackeurs Sans Frontieres - build sources - ${VERSION_CONFIG}_${BUILD_DATE}.tar.xz'
* ∀ you can build your own image by:
 	1. using openSUSE
 	2. having "kiwi" and "kiwi-desc-isoboot" packages installed
 	3. editing files, starting from 'source/*' and 'create_appliance.sh'. or not
 	4. running `create_appliance.sh`
 	5. waiting quite a bit

* ∀ the process of development for this project is like this:
 	01. _future_ release version is set in 'source/version'
 	02. desired functional changes are made
 	03. package lists are sorted via `config/sort.sh`, gitignore is generated via `data/common-userfiles_1-generate-gitignore.sh` and then changes are committed
 	04. image is build via `create_appliance.sh`
 	05. image is booted on real hardware and tested, maybe also in virtual hardware
 	06. bugs and insufficiencies are noted/reported/filed
 	07. fixes made
 	08. new image is tested and steps 6-7-8 are repeated until condition is satisfactory
 	09. the image that deemed satisfactory is considered as current release, `git tag -a` is issued with "future", now current, version
 	10. everything is repeated
