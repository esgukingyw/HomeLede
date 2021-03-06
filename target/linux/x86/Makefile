#
# Copyright (C) 2006-2011 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
include $(TOPDIR)/rules.mk

ARCH:=i386
BOARD:=x86
BOARDNAME:=x86
FEATURES:=squashfs vdi vmdk pcmcia fpu
SUBTARGETS:=64 generic zen legacy geode 
MAINTAINER:=Felix Fietkau <nbd@nbd.name>

KERNEL_PATCHVER:=4.19

KERNELNAME:=bzImage

include $(INCLUDE_DIR)/target.mk

# \
DEFAULT_PACKAGES += partx-utils mkf2fs fdisk e2fsprogs wpad kmod-usb-hid kmod-mmc-spi kmod-sdhci \
kmod-ath5k kmod-ath9k kmod-ath9k-htc kmod-ath10k kmod-rt2800-usb kmod-e1000e kmod-igb kmod-igbvf kmod-ixgbe kmod-pcnet32 kmod-tulip kmod-vmxnet3 kmod-i40e kmod-i40evf kmod-r8125 kmod-8139cp kmod-8139too kmod-fs-f2fs \
htop lm-sensors autocore automount autosamba luci-app-ipsec-vpnd luci-proto-bonding luci-app-unblockmusic luci-app-zerotier luci-app-xlnetacc ddns-scripts_aliyun ddns-scripts_dnspod ca-certificates \
luci-app-airplay2 luci-app-music-remote-center luci-app-qbittorrent luci-app-amule luci-app-openvpn-server \
ath10k-firmware-qca988x ath10k-firmware-qca9888 ath10k-firmware-qca9984 brcmfmac-firmware-43602a1-pcie \
kmod-sound-hda-core kmod-sound-hda-codec-realtek kmod-sound-hda-codec-via kmod-sound-via82xx kmod-sound-hda-intel kmod-sound-hda-codec-hdmi kmod-sound-i8x0 kmod-usb-audio \
kmod-usb-net kmod-usb-net-asix kmod-usb-net-asix-ax88179 kmod-usb-net-rtl8150 kmod-usb-net-rtl8152 kmod-r8168 kmod-mlx4-core kmod-mlx5-core


# Home Lede default x86 packages
DEFAULT_PACKAGES += partx-utils mkf2fs fdisk e2fsprogs wpad kmod-usb-hid kmod-mmc-spi kmod-sdhci \
kmod-ath5k kmod-ath9k kmod-ath9k-htc kmod-ath10k kmod-rt2800-usb kmod-e1000e kmod-igb kmod-igbvf kmod-ixgbe kmod-pcnet32 kmod-tulip kmod-vmxnet3 kmod-i40e kmod-i40evf kmod-r8125 kmod-8139cp kmod-8139too kmod-fs-f2fs \
htop lm-sensors luci-proto-bonding \
ath10k-firmware-qca988x ath10k-firmware-qca9888 ath10k-firmware-qca9984 brcmfmac-firmware-43602a1-pcie \
kmod-sound-hda-core kmod-sound-hda-codec-realtek kmod-sound-hda-codec-via kmod-sound-via82xx kmod-sound-hda-intel kmod-sound-hda-codec-hdmi kmod-sound-i8x0 kmod-usb-audio \
kmod-usb-net kmod-usb-net-asix kmod-usb-net-asix-ax88179 kmod-usb-net-rtl8150 kmod-usb-net-rtl8152 kmod-r8168 \
kmod-nls-cp936 kmod-nls-utf8 \
autocore \
homelede-autoconfig \
docker-ce open-vm-tools \
bind-dig subweb unrar unzip dmesg p7zip \
luci-app-aria2 luci-app-kodexplorer \
luci-app-hd-idle automount autosamba \
luci-theme-infinityfreedom luci-theme-argon-dark-mod luci-theme-netgear luci-theme-opentomato luci-theme-opentomcat \
ipv6helper \
luci-app-accesscontrol luci-app-control-timewol luci-app-control-webrestriction luci-app-control-weburl \
luci-app-samba luci-app-cifs-mount  \
luci-app-dockerman luci-app-hd-idle luci-app-strongswanInDocker \
strongswan strongswan-charon strongswan-default strongswan-ipsec strongswan-minimal strongswan-mod-aes strongswan-mod-attr strongswan-mod-connmark strongswan-mod-constraints strongswan-mod-des strongswan-mod-dhcp strongswan-mod-dnskey strongswan-mod-eap-mschapv2 strongswan-mod-farp strongswan-mod-fips-prf strongswan-mod-gmp strongswan-mod-hmac strongswan-mod-kernel-netlink strongswan-mod-md4 strongswan-mod-md5 strongswan-mod-nonce strongswan-mod-pem strongswan-mod-pgp strongswan-mod-pkcs1 strongswan-mod-pubkey strongswan-mod-random strongswan-mod-rc2 strongswan-mod-resolve strongswan-mod-revocation strongswan-mod-sha1 strongswan-mod-sha2 strongswan-mod-socket-default strongswan-mod-sshkey strongswan-mod-stroke strongswan-mod-updown strongswan-mod-x509 strongswan-mod-xauth-generic strongswan-mod-xcbc \
luci-app-ipsec-vpnserver-manyusers \
ppp-mod-pppoa ppp-mod-pppoe ppp-mod-pppol2tp ppp-mod-pptp pppossh xl2tpd 


$(eval $(call BuildTarget))

$(eval $(call $(if $(CONFIG_TARGET_ROOTFS_ISO),RequireCommand,Ignore),mkisofs, \
   	Please install mkisofs. \
))
