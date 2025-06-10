# Troubleshooting

## Content

- [Install missing UE5 Fab Plugin (Linux)](#install-missing-ue5-fab-plugin-linux)

## Install missing UE5 Fab Plugin (Linux)

Download the Fab plugin `Linux_Fab_5.3.0_0.0.4.zip` from the [official download page](https://www.unrealengine.com/en-US/linux).

Move the downloaded `.zip` file in the `UnrealEngine` folder, where UE is installed.

```bash
$ cd UnrealEngine
$ ls
Engine
FeaturePacks
Linux_Fab_5.3.0_0.0.4.zip  # <--
...
```

Remove existing outdated versions of the Fab plugin if any.

```bash
rm -rf Engine/Plugins/Fab
```

> [!NOTE]
> If you are using a source build, please run `make`  again to let the compilation tools know that the Fab plugin has been removed

Unzip the downloaded Fab plugin.

```bash
unzip Linux_Fab_5.3.0_0.0.4.zip
```

> [!NOTE]
> If you are using a source build, you must run the compilation again

```bash
make
```
