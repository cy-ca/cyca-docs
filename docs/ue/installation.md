# UE Installation

## Content

- [Install from Source](#install-from-source)
  - [Ubuntu](#ubuntu-source-install)

## Install from Source

### Ubuntu (Source Install)

Duraion: 2-3hrs

**Prerequisite**

- Ubuntu 22.04
- Quad-core Intel or AMD, 2.5 GHz or faster
- 32 GB RAM
- GeForce 2080
- Graphics RAM >8GB

**Install Build Dependencies**

Install `mono` as dependencies required for compilation

```bash
sudo apt install mono-devel
```

**Access to Source Code**

Follow [the official guide](https://github.com/EpicGames/Signup) to obtain access to the repository.

**Download Source Code**

After obtaining access to the GitHub Repository (<https://github.com/EpicGames/UnrealEngine>).

Proceed to download the source code. This will take a while (20-30min).

```bash
git clone git@github.com:EpicGames/UnrealEngine.git --branch 5.3.2-release
```

Run the `Setup.sh`, make sure you have a good Internet connection.

```bash
cd UnrealEngine
./Setup.sh
```

The script will try to install additional packages (for certain distributions) and download precompiled binaries of third party libraries. It will also build one of the libraries on your system (LinuxNativeDialogs or LND for short).

Generate `Makefile` (and `CMakeLists.txt`)

```bash
./GenerateProjectFiles.sh
```

**Compilation**

To compile simply run

```bash
make
```

If you intend to develop the editor, you can build a debug configuration of it:

```bash
make UnrealEditor-Linux-Debug
```

(note that it will still use development ShaderCompileWorker / UnrealLightmass). This configuration runs much slower.

If you want to rebuild the editor from scatch, you can use

```bash
make UnrealEditor ARGS="-clean" && make UnrealEditor
```

**Run**

To run the Unreal Editor

```bash
cd Engine/Binaries/Linux
./UnrealEditor
```

