# 24.1.0

1. Add "Parse pat". (Upload local pat, parse and compile, suitable for offline and special version numbers.)
2. Fix an issue where "Try to recovery a DSM installed system" may not find DSM system.
3. Fix page stretching issue, And add some prompt message.
4. fix emmc, When mmc is not used as bootloader disk and system disk, the mmc driver is automatically removed to prevent repeated hot swapping..
5. Update zh_TW.po, Thanks @marchfun1
6. Addons:
   * update eudev.
   * modify addincards. (remove 'updated usb.map')
   * add expands.(Expanded miscellaneous, updated usb.map, ca-certificates.crt, etc.)
   * other
7. modules and lkms just align the version numbers, there is no actual change.

Full Changelog: compare/23.12.10...24.1.0

# 23.12.10

1. Add web file management.
2. Fix mmc formatting stuck.
3. Add "Custom patch script".
4. Addons:
   * update hdddb, Thanks @007revad
   * Fix disks.(Fix possible disk loss issues for all models.)
5. modules:
   * Fix mpt3sas.(Fix possible disk loss issues for not-DT models.)

# 23.12.9

1. Fix iwlwifi (RR).
2. Fix EMMC as the system disk.(mvove to Advanced Menu, This feature is still not perfect)
3. Fix some typo and add some prompt.
4. modules:
   * Fix sdhci for 4.x.(test)
   * Fix panic of CFG80211.
5. addons:
   * Fix RS1619xs+ of nvmecache.
   * Fix photosfacepatch.
   * Update eudev.

Full Changelog: compare/23.12.8...23.12.9

# 23.12.8

1. add  RAID/VIRTIO information to "Show SATA(s)"
2. Modify the parameters of kexec.(test MEM error)
3. add SA3600.
4. Optimize cmdline & synoinfo of all models.
5. Update zh_TW.po, Thanks @marchfun1
6. addons:
   * update hdddb. Thanks @007revad
7. modules:
   * fix mpt3sas, (only for FS6400,HD6500, and further debugging required)
   * fix virtio_scsi, virtio_blk (only virtio disk)
   * fix megasas_sas, (Fix SA6400 support for LSI SAS 3108 (only JBOD))
 8. Other.

**Full Changelog**: compare/23.12.7...23.12.8


# 23.12.7

1. fix some typo.
2. Allow small files to be uploaded via the web.
3. add support ext4 for rack models.
4. Add EMMC as the system installation disk (synoinfo).
5. addons:
   * update disks. Fix the problem that the bootloader disk is still visible during emmc/nvme boot.
   * update hdddb. Thanks @007revad
   * modify nvmecache. Fix the problem that hardware changes cannot will updated.

**Full Changelog**: compare/23.12.6...23.12.7


# 23.12.6

1. addons:
   * add photosfacepatch. Thanks @jinlife
   * update hdddb. Thanks @007revad
2. modules:
   * fix it87.
   * fix iwlwifi. (Still not working, further repairs are needed)
   * add mvsas.

**Full Changelog**: compare/23.12.5...23.12.6


# 23.12.5

1. Optimize rr kernel module.
2. Remove web support for upload function.
3. add FS6400 and HD6500 model.
4. modules:
    * update it87, bnx2x.

**Full Changelog**: compare/23.12.4...23.12.5


# 23.12.4

1. fix something typo.
2. add "root=/dev/ram" (不知道是否可以缓解"VFS: Cannot open root device "(null)" or unknown-block(1,0): error -6" 的问题).
3. add "Clone bootloader disk to another disk".
4. modules:
   * add 9p and 9pnet_virtio (only for 7.2)

**Full Changelog**: compare/23.12.3...23.12.4


# 23.12.3

1. update translate ( zh_TW Thanks @marchfun1).
2. add updateall.
3. r8169_lk reinclude r8168.
4. Update i915 to I915-23.8.20-dsm-3. Thanks @MoetaYuko

**Full Changelog**: compare/23.12.2...23.12.3


# 23.12.2

1. fix flags of denverton(DS1819+,DS2419+).
2. add "Force enable telnet of DSM system".
4. add Changing password will force account activation.
5. default zh_CN.UTF-8.
6. add Regular match file name for "Local upload".
7. addons:
   * update codecpatch, Thanks @xbl3 @wirgen
   * update hdddb, nvmevolume, Thanks @007revad

**Full Changelog**: compare/23.12.1...23.12.2


# 23.12.1

 ≈ 23.11.10 ( buildroot updated 3Mb)


# 23.12.0

del...

# ==============================================


# 23.11.10

1. ⚠ RR system kernel upgraded to 6.4.
2. ⚠ eudev upgraded to v3.2.14.
3. fix acpid.service startup failure. Thanks @Promix953
4. fix kvm-amd.
5. modify r8169_lk (Further reducing coupling to r8168.)
6. fix gtt related issues of i915(epyc7002) .  Thanks @MoetaYuko
7. fix support for 4k displays.

**Full Changelog**: #23.11.8...23.11.10



PS:  
对不住各位，最近可能假酒喝多了，总是犯一些低级错误...
Sorry everyone, I may have been drinking too much fake alcohol lately and always making some basic mistakes...


# 23.11.9

del...


# 23.11.8

1. release 23.11.7
2. update i915 for epyc7002)(auto enable_guc). (Thanks @MoetaYuko )
3. Fixed the issue where the status bar still displays 'no build' after build.
4. Theoretically, mmc boot is supported (test by yourself)

**Full Changelog**: #23.11.7...23.11.8


# 23.11.7

1. modules:
    * add mmc driver(sdhci-pci)
    * add hwmon driver(lm75,lm90,lm95245,adm1021,it87,jc42)
    * add 9pnet
    * update r8168, r8125(disable ASPM)
    * other...
2. addons:
    * update cpuinfo (thanks @FOXBI @arabezar)
    * update dbgutils
    * update disks
3. add mmc disk related operations.
4. other.

Warning, there is a problem with wifi in this version. If there is a wifi network card, it may crash or the network may freeze.
警告，此版本中存在 wifi 問題。 如果有wifi網路卡，可能會當機或網路卡住。

**Full Changelog**: #23.11.6...23.11.7


# 23.11.6

1. 修复 无网卡时的错误提示信息.
2. update zh_TW (Thanks @marchfun1 )
3. modules:
    * Add i915 for epyc7002. (Thanks @MoetaYuko )
    * update i40e v2.20.12
    * update r8125 v9.012.03

**Full Changelog**: #23.11.4...23.11.6


PS：
我可能喝了假酒.~


# 23.11.5

del..

# 23.11.4

1. fix sa6400 no-Serial port.
2. add wireless connect for RR.
3. modules:
    * update intel ethernet driver.
    * add wireguard
4. addons:
    * fix possible disk loss issue.
    * rewrite nvme disk related logic.

**Full Changelog**: #23.11.3...23.11.4



# 23.11.3

1. modules:
    * add aacraid
2. addons:
    * fix wireless. (Sorry, due to rush, the 23.11.2 was not packaged.)

PS:
### About wireless:
1. 因为官方 在 DSM7 中删除了 wireless 相关的 GUI，所以 wireless 只能通过 ssh 进行开启。
2. 关于支持的型号，由于环境有限 并未对所有型号进行测试，请自行测试。
RTL81xx 的网卡 (all models)
RTL88xx 的网卡 (only sa6400)
Intel® Wireless-AC xxxx (all models)
Intel® Wireless-AX 2xx (only sa6400)
MediaTek MT7601u  (all models)

**Full Changelog**: #23.11.2...23.11.3


# 23.11.2

1. fix netif_num, 
   When only mac1 is filled in, netif_num is 1. When mac1 and mac2 are filled in, netif_num is 2. The actual number of network cards does not matter.
2. fix reset passwd.
3. Addons:
   * update acpid. 
   * add wireless.
4. modules:
   * other.

PS:
QEMU Guest Agent (`https://spk7.imnks.com/`)


**Full Changelog**: #23.11.1...23.11.2


# 23.11.1

1. 修改 "重置密码" 会自动去除 "验证"
2. 修改 "HDD sort" 默认为 false.
3. add wifi 驱动.
4. 更新 megaraid_sas 驱动 (理论支持 LSI SAS3108 和更高)。
5. 增加 SA6400 对 HBA 的支持.（感谢 @jim3ma）
6. 修复 i915le10th 丢失的id.

* 请同步更新 插件 和 模块.

PS:
 * 随着 PAT 越来越大，驱动也越来越多,1GB的镜像 编译时空间可能不足，物理设备会自动扩展P3分区，虚拟镜像请优先使用4GB版本.
----

1. Modifying "Reset DSM system password" will automatically remove "SecureSignIn"
2. Modify "HDD sort" default to false.
3. add wifi driver.
4. Update the megaraid_sas driver (theoretically supports LSI SAS3108 and higher).
5. Add SA6400 support for HBA. (Thanks to @jim3ma)
6. Fix the missing id of i915le10th.

* Please update addons and modules simultaneously

PS:
 * As PAT gets larger and larger, there are more and more drivers,The 1GB image may not have enough space during compilation. The physical device will automatically expand the P3 partition. Please give priority to the 4GB version for virtual images.

----

**Full Changelog**: #23.11.0...23.11.1




# 23.10.10

1. 修复sata 安装 SA6400 引导盘被格式化的问题
2. 修复 cmdline/synoinfo 添加不进去的问题。
3. add mac2，

请同步更新 插件.

PS：
因为底层改动较大，我自己很难全部测试稳定，近期只能根据用户反馈，较为严重的问题都会修改后及时发布。所以更新比较频繁，如果你当前没有太大问题，暂时可以不必更新。

---
1. Fix the problem of the SA6400 boot disk being formatted during SATA installation
2. Fix the problem that cmdline/synoinfo cannot be added.
3. add mac2，

Please update the addons simultaneously.

PS:
Because the underlying changes are relatively large, it is difficult for me to test all the stability myself. In the near future, I can only rely on user feedback. More serious problems will be modified and released in a timely manner. Therefore, updates are relatively frequent. If you don’t have major problems at the moment, you don’t need to update for the time being.

**Full Changelog**: #23.10.9...23.11.0



# 23.10.9

1. 修复编译 dialog 显示乱码
2. 增加常用的 cmdline/synoinfo 提示
3. 修复 sa6400 找不到硬盘
4. 修复 某些情况下 磁盘驱动器第一位的银盘丢失
5. 增加 r8169_lk.ko（旧版本的r8169）

 * 请同步更新 插件 和 模块
----

1. Fix build dialog displaying garbled characters
2. Add commonly used cmdline/synoinfo prompts
3. Fix sa6400 cannot find hard disk
4. Fix In some cases, the first disk of the disk drive is missing
5. Added r8169_lk.ko (old version of r8169)

 * Please update addons and modules simultaneously

**Full Changelog**: #23.10.8...23.10.9




# 23.10.8

1. Fix staying at %99.

**Full Changelog**: #23.10.7...23.10.8


# 23.10.7

1. fix RecoveryDSM
2. fix wol (test)
3. addons:
   * dbgutils 
   * other

**Full Changelog**: #23.10.6...23.10.7


# 23.10.6

1. 发布 #/23.10.5
2. add "HDD 排序"
    * true - dts 包含所有硬盘端口。 优点是支持热插拔，缺点是硬盘排序不连续。
    * false - 只识别插入的硬盘，（原方案）
    （PS：这个名字好像有点与实际情况不符，我可能会在下个版本中更改）

----

1. release #/23.10.5
2. add "HDD sort"
    * true - dts contains all hdd ports. The advantage is that it supports hot swapping, but the disadvantage is that the hard disk sorting is discontinuous.
    * false -- only recognize the inserted hard disk, (original solution)
    (PS: The name seems a bit inconsistent with the actual situation, I will change it in the next version)

**Full Changelog**: #23.10.5...23.10.6




# 23.10.5

已调整架构 以支持热修改，插件卸载等功能，不过当前仍未实现。
虽然UI看上去变化不大，但是逻辑上修改量很大。

以下为较前一版的修复
1. 支持 Nvme 盘引导. (只是引导盘可为 Nvme.)
2. 支持 sata 安装SA6400.
3. 修改 Logo 为 QR.
4. 优化 r8152/r8168/r8169 驱动 (RR and DSM).
5. 添加 r8125_v9, bnx2x_mod 驱动（DSM）
    ```
       bnx2x        --> 正常
       bnx2x_mod    --> 添加 2.5g 支持
       r8125.ko     --> v9.011.01
       r8125_v9.ko  --> v9.009.02
    ```
6. 其他修复.
7. :warning: RebootToArpl 更名为 RebootToLoader.
8. :warning: Arpl-i18n 暂时不能直接升级到 RR. 
    因为很多底层处理不一样，我不建议直接升级到RR，
    当然如果大部分人仍想直接升级，我会考虑做一个升级包。

----

The architecture has been adjusted to support hot modification, plug-in uninstallation and other functions, but it is not yet implemented.
Although the UI does not seem to have changed much, the logic has been greatly modified.

The following are the fixes compared to the previous version
1. Support Nvme disk boot. (Only the boot disk can be Nvme.)
2. Support sata installation SA6400.
3. Modify the Logo to QR.
4. Optimize r8152/r8168/r8169 driver (RR and DSM).
5. Add r8125_v9, bnx2x_mod driver (DSM)
    ```
        bnx2x        --> normal
        bnx2x_mod    --> Add 2.5g support
        r8125.ko     --> v9.011.01
        r8125_v9.ko  --> v9.009.02
    ```
6. Other fixes.
7. :warning: RebootToArpl was renamed to RebootToLoader.
8. :warning: Currently Arpl-i18n cannot be directly upgraded to RR.
    Because many underlying processes are different, I don’t recommend upgrading directly to RR.
    Of course, if most people still want to upgrade directly, I will consider making an upgrade package.
----

**Full Changelog**: #23.10.4...23.10.5


Add:
arpl-i18n to rr:
1. update arpl-i18n to version 23.10.4
2. curl -kL https://github.com/syno-community/rr/releases/download/23.12.8/arpl-i18n-23.10.4-to-rr-23.10.5.sh | bash
3. Go to 'menu.sh -> update menu' immediately to update.(enable 'Pre Release')



# 23.10.4

1. add RS2423+.
2. add support for tg3 NIC.
3. Other optimizations.

**Full Changelog**: #/23.10.3...23.10.4

PS:
This is the last arpl-i18n version.
see you in the next product.


<details><summary></summary>
lol, Let me lay my cards on the table,
It will continue under a new name and gradually change focus.
</details>

add:
:warning:
There is a serious problem with addons versions after v23.9.7 (inclusive).
When installing DSM 7.1(inclusive) and below, an error message will be reported, saying that the hard disk cannot be found, cannot be connected, etc.
Because it was discovered late, it will be dealt with uniformly after the RR revision, everyone knows!


# 23.10.3

1. fix UI(progressbox )多个显示撕裂的问题.
2. fix “内核恐慌时重新启动” 对 直接启动的兼容. (23.10.2).
3. addons:
   * add sortnetif (网卡排序插件) .(23.10.2 for details.)
   * update misc:  添加依赖.
   * update nvmecache: 修复 DS918+ DS1019+ DS1621xs+ 开启nvmecache插件， webUI 挂掉(登不进去)的问题.
   * update wol: 多网卡支持.
----

1. fix the tearing issue in the format disk UI display(progressbox ),
2. Fix "reboot on kernel panic" compatibility with direct boot. (23.10.2).
3. addons:
   * add sortnetif (network card sorting). (23.10.2 for details.).
   * update misc:  add depends.
   * update nvmecache: Fix the webUI hangs (cannot log in) when the nvmecache addons is enabled of  DS918+ DS1019+ DS1621xs+.
   * update wol: Multiple network card support.


**Full Changelog**: #/23.10.2...23.10.3


# 23.10.2

1. fix 格式化磁盘UI显示撕裂问题, 
2. fix “内核恐慌时重新启动” 对 直接启动的兼容.
3. addons:
   * add sortnetif （网卡排序插件）.
         参数:
         * null: 以busid排序
         * macs：优先排序指定的 mac对应的网卡,  (eg: 112233445566,112233445577) (有无冒号也皆可，也不区分大小写，逗号分割，或者空格分割加双引号)

----

1. fix the tearing issue in the format disk UI display,
2. Fix "reboot on kernel panic" compatibility with direct boot.
3. addons (pre):
    * add sortnetif (network card sorting plug-in).
          parameter:
          * null: Sort by busid
          * macs: Prioritize the network card corresponding to the specified mac, (eg: 112233445566, 112233445577) (it can be used with or without a colon, it is not case sensitive, comma separation, or space separation plus double quotes)

**Full Changelog**: #/23.10.1...23.10.2

PS: 内核恐慌≈内核噶了，别问了，好不


# 23.10.1

1. 添加 “内核恐慌时重新启动”
   当内核恐慌时, 它会自动重新启动, 以缓解偶尔出现的内核死机.
 （升级引导不会默认启用, 请手动打开; 全新安装将默认启用.）
2. 添加 "兼容性判断".
   根据当前硬件环境确定模型的兼容性。
3. 优化 cmdline 逻辑。
   调高用户cmdline的优先级，使其能够覆盖固有的cmdline。
4. 优化大量提示信息. Thx 豪哥@marchfun1 对 zh_TW 的翻译支持.
5. addons:
   * 更新 nvmecache.
---

1. add "Reboot on kernel panic".
   When a kernel panic occurs, it will automatically reboot to alleviate occasional kernel panic.
   (Upgrade bootloader will not be enabled, please manually enable it, new write bootloader will be enabled by default.)
2. add "Compatibility judgment“.
   Determine the compatibility of the model based on the current hardware environment.
3. Optimize cmdline logic.
   Increase the priority of the user set cmdline to allow it to override the inherent cmdline.
4. Optimize a large amount of prompt information. Thx 豪哥@marchfun1 for zh_TW Translation support.
5. addons:
   * update nvmecache.

**Full Changelog**: #/23.10.0...23.10.1


# 23.10.0

1. update SN of DS224+, DS1522+, SA3200D, SA3400D, Thanks @OrpheeGT
2. update zh_CN, Thanks @sumingyd 
3. update zh_TW, Thanks @豪客幫
4. add edit grub.cfg


**Full Changelog**: #/23.9.7...23.10.0


# 23.9.7

1. 添加 DS224+, DS1522+, SA3410, SA3610
2. 修改mac相关:
   2.1. 取消了激活 mac 和 物理网卡的关联性, mac参数仅作为洗全白用，不会设置到物理网卡.
        这缓解了一些网卡在修改mac后无法dhcp的问题.
   2.2. 取消了网卡数和物理网卡的关联, 
        这缓解了USB网卡可能需要手动 up 的问题.
3. addons:
   * update storagepanel (v23.9.6)
   * update misc (v23.9.7)
   * update reboottoarpl (v23.9.7)
4. lkms:
   * 取消了cmdline参数校验, 允许 mac* 个数和 netif_num 不一致.

PS:  
本次修改较大，由于明天为中秋佳节，因此提前发出。同时祝大家节日快乐，身体健康！

add:  
很抱歉，因为取消了mac的关联关系，所以 我统一设置了随机的mac1，如果是旧版本升级到23.9.7 mac1会变为随机mac，如果你之前填写了自定义的mac 请在升级后检查并重新设置。

----

1. Add DS224+, DS1522+, SA3410, SA3610
2. Modify MAC related:
   2.1. The association between activating the MAC and the physical network card has been cancelled, and the MAC parameters are only used for authentication and will not be set to the physical network card.
        This alleviates the issue of some network cards not being able to dhcp ip after modifying the mac.
   2.2. The association between the number of network cards and physical network cards has been cancelled,
        This alleviates the issue of the USB network card needing to be manually up.

3. Addins:
   * Update storagepanel (v23.9.6)
   * Update misc (v23.9.7)
   * Update reboottoarpl (v23.9.7)

4. lkms:
   * Canceled cmdline parameter validation, allowing for mac * count and netif_num is inconsistent

PS:  
This modification is big and will be sent out in advance as tomorrow is the Mid Autumn Festival. At the same time, I wish everyone a happy holiday and good health!

Add:
Sorry, because I canceled the association of mac, I set a random mac1. If the old version is upgraded to 23.9.7 mac1 will become a random mac. If you have filled in a custom mac before, please check it after the upgrade. and reset.

**Full Changelog**: #/23.9.6...23.9.7