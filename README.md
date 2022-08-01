# fakertc
Save real-time clock on small devices running FreeBSD like the Raspberry Pi.

Computers without a real-time clock will have the clock way off on 
boot. NTP can be used to correct the clock. But when network setup
depends on valid certificates for DNSsec or IPsec the time is not
allowed to be off too much.
This utility can help by saving the date and time on shutdown and
restoring it on startup. The clock is only off as long as the system
took to reboot.
This also helps to logs to not go backwards in time.

NB: If you are running UFS-on-root the system already gets the time
from the UFS superblock. ZFS does not have this feature.
NB2: The idea of this utility came from https://lists.freebsd.org/archives/freebsd-arm/2022-July/001522.html
