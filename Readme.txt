virtualbox usb(LINUX LIVE ISO)開機

資料來源: https://anal02.pixnet.net/blog/post/113609927-virtualbox%E4%B8%AD%E4%BD%BF%E7%94%A8usb%E9%96%8B%E6%A9%9F%E7%9A%84%E6%96%B9%E6%B3%95%2C%E5%A6%82%E4%BD%9C%E6%A5%AD%E7%B3%BB%E7%B5%B1%E6%88%96%E8%87%AA


01.首先先把命令提示字元開啟，要用系統管理員身分執行

02.切換目錄
cd c:\Program Files\Oracle\VirtualBox

03.確認開機USB是系統第 [X] 顆硬碟

04.產生vmdk檔
#--VBoxManage internalcommands createrawvmdk -filename D:\VirtualBox\usb.vmdk -rawdisk \\.\PhysicalDrive[X]
VBoxManage internalcommands createrawvmdk -filename D:\VirtualBox\usb.vmdk -rawdisk \\.\PhysicalDrive2

05.接下來用系統管理員身分去執行virtualbox

06.選擇vmdk作為開機硬碟