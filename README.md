# NetClip

Copy things in one device and paste in another. This is a command line tool, and copying using right click -> copy will not work here. Think of it more as a [pbcopy](https://ss64.com/mac/pbcopy.html), [pbpaste](https://ss64.com/mac/pbpaste.html) from MacOS (spoiler alert: it actually uses these commands for the macos scripts).

## Pre-requisites

This depends on `scp` to copy files over the network, so make sure devices are SSH-able. 

## Installation

Just copy over the scripts for your operating system to `/usr/local/bin`.

### For Linux

For linux the program used for accessing clipboard data is `xsel`, so make sure to install that otherwise this won't work.

### For MacOS

For macOS the program used to access clipboard is `pbcopy` and `pbpaste` which ship with the macOS installations. 

### For Windows

Just switch to macOS or linux already.

## Usage

- Copy from one device:

```bash
echo "Hello from one device" | netcopy
```

- Paste in another device:

```bash
netpaste <IP>
```

Where `<IP>` is the IP address of the host from where stuff is to be copied. 