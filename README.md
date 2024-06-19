
  <h3 align="center">Fortnite Cheatarchive</h3>

  <p align="center">
    <a href="[https://discord.gg/nexustools](https://discord.gg/V6uAKyu4KP)">Discord</a>
  </p>

  <h3 align="center">Connect with me:</h3>
<p align="center">
<a href="https://discord.com/users/1202026685789393026" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/discord.svg" alt="balls" height="30" 
</p>

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

```sh 
Some leaked sources. Fortnite ext/int, Spoofer perm/temp Valorant ext/int.
```

> [!Warning]
> Please make sure you doublecheck the sources for rats. Look closely into proj file and drivers

> [!Note]
> All of the uploaded sources on this repo are leaked so do not expect someting UD you will have to change driver and overall code to make it UD!


# Usefull stuff

> https://github.com/ReadProcessMemory/fortnite-offsets-sdk

> https://github.com/paysonism/Fortnite-Offsets

# Credits 

> Enigmasolutions: [https://discord.gg/enigmacheats](https://discord.gg/V6uAKyu4KP)


# Tutorials

> https://www.youtube.com/@pastingschool

> https://www.youtube.com/@hfromcapware

# The sources are heavily outdated after the newest Update so you will have to implement this into your paste to get it working.
Main.cpp: (code to read out "dynamic_uworld" this it very important!)
```c++
int64 va_text = 0;
for (int i = 0; i < 25; i++)
	if ((driver.read<int32>(base_address + (i * 0x1000) + 0x250)) == 0x260E020B)
	{
		va_text = base_address + ((i + 1) * 0x1000);
		dynamic_uworld = offset::uworld + va_text; //offset::uworld or 0x129DEDD8 (19.06.24)
	}
```
Cache.h (read uworld using the premade "dynamic_uworld")
```c++
arrays->uworld = driver.read<uintptr_t>(dynamic_uworld);
```

Offsets.h (just definition (you can also define it somewhere else))
```c++
__int64 dynamic_uworld;
```








