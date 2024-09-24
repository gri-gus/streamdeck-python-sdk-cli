<p align="center">
    <a href="https://pypi.org/project/streamdeck-sdk-cli" target="_blank">
        <img src="https://img.shields.io/pypi/v/streamdeck-sdk-cli" alt="PyPI">
    </a>
    <a href="https://pypi.org/project/streamdeck-sdk-cli" target="_blank">
        <img src="https://static.pepy.tech/badge/streamdeck-sdk-cli" alt="PyPI">
    </a>
    <a href="https://opensource.org/licenses/Apache-2.0" target="_blank">
        <img src="https://img.shields.io/badge/License-Apache_2.0-blue.svg" alt="Apache">
    </a>
    <a href="https://docs.elgato.com/sdk" target="_blank">
        <img src="https://badgen.net/badge/Elgato/doc/blue" alt="Elgato">
    </a>
</p>

# streamdeck-python-sdk-cli

Command Line Interface for [streamdeck-python-sdk](https://github.com/gri-gus/streamdeck-python-sdk).

**PyPi**: https://pypi.org/project/streamdeck-sdk-cli

**Supported operating systems:**

* MacOS: 10.14 or later
* Windows: 10 or later

**Supported Python versions:** 3.8 or later

## Installation

> ⚠️ For correct operation on Windows, it is recommended to enable `LongPaths` support in
> the system: [manual](https://www.backupery.com/how-to-enable-ntfs-long-paths-in-windows/).
> Without this setting, problems with installation and use may occur!

```shell
pip install streamdeck-sdk-cli
```

## Usage

### Start Project

Creates a project template for [streamdeck-python-sdk](https://github.com/gri-gus/streamdeck-python-sdk).

```shell
streamdeck_sdk startproject
```

### Packaging

Package the project into a `.streamDeckPlugin` file.

> ⚠️ The `requirements.txt` file should not contain the `streamdeck-sdk-*` libraries. If there are any, remove them.

```shell
streamdeck_sdk build -i com.bestdeveloper.mytestplugin.sdPlugin
```

`-i` : Project folder for packaging.

⚠️ If you are using Windows and receive an error, then use the command:

```shell
streamdeck_sdk build -i com.bestdeveloper.mytestplugin.sdPlugin -F
```

`-F` : Forced packaging through an unofficial builder.

### Update the files that are used to run the plugin

The files `init.py`, `run.bat`, `run.sh` will be updated.

```shell
streamdeck_sdk updatelaunch -i com.bestdeveloper.mytestplugin.sdPlugin
```

`-i` : Project folder for packaging.
