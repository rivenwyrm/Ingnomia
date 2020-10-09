# README #

## How do I get set up? ##

The following steps describe how to compile the code and get the game running on Windows and Linux.

Note! Building on Mac is currently not possible. Certain features in the renderer require OpenGL4.3.

### Dependencies ###

* Microsoft Visual Studio 2019, the community edition is free
* OpenGL 4.3 - Mac is not a supported compilation platform since it has deprecated OpenGL
* Qt 5.14.1
* Qt [vs addin](http://download.qt.io/official_releases/vsaddin/2.5.2/) (recommended)
* [Noesis Gui](https://www.noesisengine.com/developers/downloads.php) 3.0.4 \
  Download the native SDK for your OS and build the NoesisApp in *Debug* configuration.
  For using Noesis in a development build, you need to get a [trial license](https://www.noesisengine.com/trial/).
* [Steam SDK](https://partner.steamgames.com/doc/sdk)
* CMake 3.16 or newer

### Build ###

```bash
cp -r "<EXISTING_INGOMIA_INSTALLATION>/content/tilesheet" /content
mkdir build && cd build
cmake .. \
-DQt5_DIR="<QTINSTALLDIR>/<ARCH>/lib/cmake/Qt5" \
-DSTEAM_SDK_ROOT="<STEAMSDKDIR>/sdk" \
-DNOESIS_ROOT="<NOESISDIR>" \
-DNOESIS_LICENSE_NAME="<TRIAL_LICENSE_NAME>" \
-DNOESIS_LICENSE_KEY="<TRIAL_LICENSE_KEY>"
```

If no errors have occured, proceed building the project with the chose build system.

## Contribution guidelines ##

Help with Ignomia is always welcome.

### Making suggestions ###

We love to hear about your ideas on this game! Please head straight to our [Discord](https://discord.gg/DCSmxVD) server and discuss them in the #suggestions channel. You might see them realized at some point.

Please don't open tickets for suggestions on your own. That is reserved for already planed features.

### Reporting bugs ###

Even if you can't contribute in code, testing and reporting bugs is just as important to us. If you find something which doesn't behave right, or even crashes, feel free to open a ticket in the bugtracker.

Please include only one bug per ticket, with a precise step-by-step instruction how to trigger, and search for open tickets on the same subject first.

If you prefer, you may also try to reproduce bugs reported by other users. The more precise informations on a bug are, the higher the chance it can be fixed.

### Code contributions ###

If you know any of C++ or WPF, you can help right away! Feel free to check for open bugs, and hop over to our [Discord](https://discord.gg/DCSmxVD) channel to get you sorted in.

Please provide your contributions in the form of a pull request, rebased onto the current head of development.

When forking the project on Github, you should add `NOESIS_LICENSE_KEY` and `NOESIS_LICENSE_NAME` as secrets in your repositories configuration under Settings/Secrets. If not provided, CI builds will fail for your fork.

#### License ####

The contents of this repository are licensed under [GNU AFFERO GENERAL PUBLIC LICENSE Version 3](LICENSE). All contributions must adhere to the terms and conditions of this license. By submitting a pull request, you attest that you own the necessary rights on the code and you will abide to the AGPL3 license.

### Who do I talk to? ###

Hop over to our [Discord](https://discord.gg/DCSmxVD) server or open a ticket please.
