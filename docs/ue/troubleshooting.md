# Troubleshooting

## Content

- [Install missing UE5 Fab Plugin (Linux)](#install-missing-ue5-fab-plugin-linux)

## Install missing UE5 Fab Plugin (Linux)

Download the Fab plugin `Linux_Fab_5.3.0_0.0.4.zip` from the [official download page](https://www.unrealengine.com/en-US/linux).

Move the downloaded `.zip` file at the same directory as the `UnrealEngine` folder, where UE is installed.

```bash
$ ls
Linux_Fab_5.3.0_0.0.4.zip
UnrealEngine
```

Remove existing outdated versions of the Fab plugin if any.

```bash
rm -rf UnrealEngine/Engine/Plugins/Fab
```

Unzip the downloaded Fab plugin.

```bash
unzip Linux_Fab_5.3.0_0.0.4.zip
```

**[Optional]** If you are using a source build, you can run the compilation again

```bash
cd UnrealEngine
make
```

