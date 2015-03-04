# Bettlefold: Bed Companion 2 Open Emulation

About
------------
This repository joins the open source MASE masterserver emulator and the source code for client hook.

Compiling MasterServer
------------
Dependencies: ```Boost, OpenSSL```

On Windows: In Visual Studio, open ```masterserver/mase_bc2.sln``` and build.
On Linux: in ```masterserver``` folder, run ```make release``` or ```make debug``` based your preference. If you run into problems, look into ```Makefile```.

Compiling ClientHook (Windows only)
------------
Open ```clienthook/msvc/Hooks.sln``` in Visual Studio and build.

Configuration
------------
The masterserver configuration files reside in the ```masterserver/Debug``` and ```masterserver/Release``` locations, same place where your compiled executables should be:
* ```config.ini``` - pretty well internally documented configuration file, the value you are going to want to change the most is ```emulator_ip```.
Some useful templates:
* ```templates/countryList``` - list of countries to choose from when registering
* ```templates/game``` - the ticker in game menu
* ```templates/termsOfService``` - The Terms of Service which show up when registering
* ```templates/termsOfService_orig``` - EA's original TOS

You also want to change ```alokal.eu``` to your own hostname/ip address in ```clienthook/msvc/BC2.cpp```

Running game
------------
0. Make sure your game is the latest, non-steam version
1. Run the masterserver
2. Copy ```dinput8.dll``` to game directory
3. Run the game, register a new account. Email don't even have look like an email (e.g. 'lolzrandom' is perfectly fine)
4. Play

Running dedicated server
------------
1. Obtain Server R32 files
2. Make sure masterserver is running
3. Copy ```dinput8.dll``` to server directory
4. Run the server, command-line is as such: ```Frost.Game.Main_Win32_Final.exe -serverInstancePath "Instance/" -mapPack2Enabled 1 -port 19567 -timeStampLogNames -region OC -heartBeatInterval 20000```

Issues
------------
* Character 'x' is forbidden in account/persona names
* passwords can't contain only 0's (e.g. 0000)

Credits
------------
* NoFaTe
* Triver
* TheDomo
* Freaky123
* Rodney
* bcool
* aluigi