Redistributed from: http://www.ahammer.ch/141

lvmcache-statistics.sh displays the LVM cache statistics in a user friendly manner

Copyright (C) 2014 Armin Hammer 

This program is free software: you can redistribute it and/or modify 
it under the terms of the GNU General Public License as published by 
the Free Software Foundation, either version 3 of the License, or (at 
your option) any later version.

This program is distributed in the hope that it will be useful, but 
WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY 
or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License 
for more details.

You should have received a copy of the GNU General Public License along 
with this program. If not, see http://www.gnu.org/licenses/.

Usage:
lvmcache-statistics.sh [lvm-device]
lvm-device: device file of the to be inspected LVM device
            if not set - the first LVM cache device will be used
 
Sample:
- lvmcache-statistics.sh
- lvmcache-statistics.sh /dev/vg00/lvol0

References
- https://www.kernel.org/doc/Documentation/device-mapper/cache.txt
- https://www.kernel.org/doc/Documentation/device-mapper/cache-policies.txt
- https://en.wikipedia.org/wiki/Dm-cache
- ftp://sources.redhat.com/pub/lvm2/WHATS_NEW
- $ man lvmcache

History:
20141220 hammerar, initial version v1.0
20151219 hammerar, complete overhaul and much more verbose v2.0
20151220 hammerar, no policy args in smq policy fixed
20160326 hammerar, bugfix lvm detection and better policy undestanding
20170915 hammerar, bugfix mg instaead of mq typo
                   missed cleaner policy

Todo:
- division by zero if you call statitics if not even 1 block is used
- fully add cleaner policy
