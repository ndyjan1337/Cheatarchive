
# Tags
```internal```
```data```
```hack```
```discord ```
```driver ```
```external ```
```ioctl ```
```cheats ```
```cracked ```
```fortnite spoofer ```
```fortnitehack ```
```fortnite-esp ```
```valorant-driver ```
```spoofer-eac ```
```spoofer-valorant ```
```fortniteexternal ```
```fortnite-driver-source ```
```fortnit-driver-leak ```
```fortnitedriver```

# Fortnite Cheatarchive

```
Some leaked sources. Fortnite ext/int, Spoofer perm/temp Valorant ext/int.
```
> [!Note]
> These sources are all leaked nothing here is "UD" or updated you will have to change some stuff to make it good.
 
> [!Warning]
> Doublecheck for rats! These sources are just reposted and sorted out (check .vcxproj file for externally downloads, .lib files)

# The sources are heavily outdated after the newest update so you will have to implement this into your paste to get it working.
> Main.cpp: (code to read out "dynamic_uworld" this it very important!)
```c++
int64 va_text = 0;
for (int i = 0; i < 25; i++)
	if ((driver.read<int32>(base_address + (i * 0x1000) + 0x250)) == 0x260E020B)
	{
		va_text = base_address + ((i + 1) * 0x1000);
		dynamic_uworld = offset::uworld + va_text; //offset::uworld or 0x129DEDD8 (19.06.24)
	}
```

> Cache.h (read uworld using the premade "dynamic_uworld")
```c++
arrays->uworld = driver.read<uintptr_t>(dynamic_uworld);
```

> Offsets.h (just definition (you can also define it somewhere else))
```c++
__int64 dynamic_uworld;
```

# Credits 

[Enigmasolutions](https://discord.gg/V6uAKyu4KP)








