
# Floconhome KB 

> This is some stuff, tips, softwares, useful web links I use for professionnal or personnal use, I agregate and share to you.

Have fun :wink: !

**Summary** _(alphabetical sort)_

- [android Activity manager (am) help](#android-activity-manager-am-help)
- [android Busybox 1.34.1-osm0sis help](#android-busybox-1341-osm0sis-help)
- [## android getprop usage](### android-getprop-usage)
- [android Package Manager (cmd package) help](#android-package-manager-cmd-package-help)
- [Ditto Clipboard Manager](#ditto-clipboard-manager)
- [Frija - Samsung firmware downloader](#frija---samsung-firmware-downloader)
- [Sublime Text](#sublime-text)
  
  
---  
  

## android Busybox 1.34.1-osm0sis help
- extracted with this script:
```shell
exec &>busybox.1.34.1-osm0sis.help.txt

for applet in $(busybox --list)
do
  echo "####################"
  echo "# $applet"
  echo "####################"
  busybox $applet --help
  echo
done
```
- go to [help file](/files/busybox.1.34.1-osm0sis.help.txt)

## android Activity manager (am) help
- extracted from Android 10 from G960FXXSHFUJ2 stock firmware on 2022-01-16, thanks to this commande line: `am -h > /data/media/0/am.help.txt`
- go to [help file](/files/am.help.txt)

## android getprop usage
- just enter `getprop` in command line to list all actives/running props with its corresponding value; output example (extract):
```shell
[ro.vendor.build.fingerprint]: [samsung/starltexx/starlte:10/QP1A.190711.020/G960FXXSHFUJ2:user/release-keys]
[ro.vendor.build.id]: [QP1A.190711.020]
[ro.vendor.build.security_patch]: []
[ro.vendor.build.tags]: [release-keys]
[ro.vendor.build.type]: [user]
[ro.vendor.build.version.incremental]: [G960FXXSHFUJ2]
[ro.vendor.build.version.release]: [10]
[ro.vendor.build.version.sdk]: [29]
[ro.vendor.build.version.sehi]: [2905]
[ro.vendor.cscsupported]: [1]
[ro.vendor.ddk.set.afbc]: [1]
[ro.vendor.epdg.support]: [true]
[ro.vendor.mg_factory_mode]: [0]
[ro.vendor.multisim.simslotcount]: [2]
[ro.vendor.product.cpu.abilist]: [arm64-v8a,armeabi-v7a,armeabi]
[ro.vendor.product.cpu.abilist32]: [armeabi-v7a,armeabi]
[ro.vendor.product.cpu.abilist64]: [arm64-v8a]
[ro.vendor.product_ship]: [true]
[ro.vendor.radio.default_network]: [9]
[ro.vendor.radio.default_network_by]: [telephony.prop_9]
[ro.vendor.sec.radio.def_network]: [9]
[ro.vendor.security.vaultkeeper.id]: [o0blqW99le22Fb1H]
[ro.vndk.version]: [29]
[ro.wifi.channels]: []
[ro.zygote]: [zygote64_32]
[ro.zygote.disable_gl_preload]: [true]
[sec.fle.encryption.status]: [decrypted]
[secmm.codecsolution.ready]: [1]
[security.ADP.policy_version]: [20191001]
[security.ADP.version]: [3.0]
[security.ASKS.policy_version]: [20200806]
[security.ASKS.rufs_enable]: [true]
```
- we can get just one prop at time by entering target prop, for example `getprop ro.vendor.build.fingerprint`:
```shell
samsung/starltexx/starlte:10/QP1A.190711.020/G960FXXSHFUJ2:user/release-keys
```
- instead of prop value, we can get type or context, useful in shell script:
  - `getprop -T ro.vendor.build.fingerprint` will return `string`
  - `getprop -Z ro.vendor.build.fingerprint` will return `u:object_r:vendor_default_prop:s0`

## android Package Manager (cmd package) help
- extracted from Android 10 from G960FXXSHFUJ2 stock firmware on 2022-01-16, thanks to this commande line: `cmd package > /data/media/0/cmd.package.help.txt`
- go to [help file](/files/cmd.package.help.txt)


## Frija - Samsung firmware downloader
- github repo: https://github.com/SlackingVeteran/frija/releases
- XDA forum link: https://forum.xda-developers.com/t/tool-frija-samsung-firmware-downloader-checker.3910594/
- a nice tool to download latest stock firmware of a samsung mobile; be careful: only latest firmware, not oldest than latest one; I use it for my phones, when I need a stock firmware to work on it or to recover my phones

![Frija main window](/screenshot/frija/frija.main.window.png)
![Frija main window](/screenshot/frija/frija.main.window.png.search.result.png)
![Frija main window](/screenshot/frija/frija.main.window.png.settings.png)
![Frija main window](/screenshot/frija/frija.settings.png)
  
## Sublime Text
- web site: https://www.sublimetext.com/
- this greatful text tool is usefull for organising note taking and project code; I use it in professionnal context to organise my notes from a folder on my computer, read some data text files; in personal context, it helps me for android project, reading text and binary file; moreover, I especially like the dark theme and the syntaxic colors theme: it is eye relaxing
- in the second screenshot, I present you what is usefull for my usage:
1. the vertical left banner helps me see my folders/files tree, quickly having a look where I want to go
1. the main window, in dark theme, with syntaxic color theme
1. the global view on the right helps me quickly navigate throw the file being displayed in the main window; I win time when I use it
1. the search location on the bottom of the window can be used to search anything in the file displayed in the main window, and more, throw the folders/files tree in the vertical left banner; I do not use it often, but when I need, it is helpful
  
![Sublime Text main window](/screenshot/sublimetext/sublimetext.main.window.png)
![Sublime Text main window with explanations](/screenshot/sublimetext/sublimetext.main.window.explanations.png)

## Ditto Clipboard Manager
- web site: https://ditto-cp.sourceforge.io/
- github repo: https://github.com/sabrogden/Ditto/
- once installed, it discreet stays in the notification bar; you call it with a keyboard shorcut, default defined on "CTRL + ù" (can be modified); it is a great tool for professionnel workers who needs to copy/paste and search for data (text, pictures, and so on) all along their wroking days; it is also a great tools in a personal use for same reason; I use it since 2017: Jean-Marc, a co-worker in the professionnal team where I was, told me about it, and since then, I do not do without it 😉
  
![Ditto main window](/screenshot/ditto/ditto.main.window.png)
  
![Ditto main window](/screenshot/ditto/ditto.notification.png)
