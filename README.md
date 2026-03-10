This is a UXP based browser that can be built and run on 10.4.11 Tiger PowerPC.
A huge thank you to the following upstreams for their work:
1. @danupser for making a browser that can be run, though not built, on 10.4.11 Tiger PowerPC (and all other MachFox contributors).
2. @Jazzzny for contributions to UXP code on Mac OS X PowerPC (and all other contributors of PowerFox).
3. @dbsoft for porting UXP to Mac OS X PowerPC (and all other contributors to White Star).
4. To the Basilisk/UXP/Pale Moon/other teams for making such a vibrant and portable Firefox fork.
5. To @theWireless, for keeping Aquafox alive and available (and all other contributors).
6. To Cameron Kaiser, for many brilliant fixes to allow Firefox to build and run on 10.4.11 Tiger PowerPC for many years (and to all other TenFourFox contributors).
7. To Mozilla, for making a great browser to fork from (and all other Firefox contributors).

To build, you will need the following:
1. A PowerPC Mac running 10.4.11 Tiger with as much RAM and disk space as you can manage (only G4 is tested currently, with 2 GB of RAM)
2. Build tools and runtime dependencies - GCC10 and Libffi are both, darwin xtools and ld64-97 +tigerrpath are build only. Other common tools may be pulled in as well.
It is recommended to get the build tools from @barracuda156's PowerPC ports. You will need to install the base from source, ideally against external curl, but that is outside the scope here.
3. You need to download the source code from here.
4. You need https://github.com/danupsher/tiger-ppc-builds/blob/main/ld64-pipeline/tiger-compat.h The default configuration assumes it is located in /extraheader/include/tiger-compat.h  It is assumed that folder is part of your top directory.
5. If building for G4, you can cd into the folder of the source code, then ./mach run and hopefully in a day or so it will finish successfully.
If building for another platform you will need to change the mozconfig. You might also need to make sure your dependencies were built for the platform you are compiling for.
Cross-compiling is outside the scope of StoneColdFox - that is our main difference from MachFox.
6. To run, ./mach run

Please raise an issue if building from source doesn't produce something runnable with ./mach run.
