# Trusted Home Feed
This feed adds Irdeto Trusted-Home Unum agent to OpenWrt builds.


Overview    
Add this feed to an OpenWrt build's *feeds.conf.default* file:

```
# Trusted-Home feed
src-git trusted-home https://github.com/HolidayCactus/trusted-home-feed.git
```
Update the local copy of the Trusted-Home feed with the OpenWrt feeds script:

```
./scripts/feeds update trusted-home
./scripts/feeds install trusted-home
```
Enable the Unum agent in *make menuconfig* under *Network*.

Build an Unum agent ipk with *make package/unum/compile*, then use *scp* to copy the ipk onto your router and use *opkg install* to install it.
