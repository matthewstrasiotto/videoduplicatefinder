# Video Duplicate Finder
Video Duplicate Finder is a cross-platform software to find duplicated video (and image) files on hard disk based on similiarity. That means unlike other duplicate finders this one does also finds duplicates which have a different resolution, frame rate and even watermarked.

# Features
- Cross-platform
- Fast scanning speed
- Ultra fast rescan
- Finds duplicate videos / images based on similarity
- Windows GUI, Linux GUI and multi-OS Console

# Requirements
FFmpeg and FFprobe is required.

# Binaries

[Latest release](https://github.com/0x90d/videoduplicatefinder/releases)

Latest build: [![Build status](https://ci.appveyor.com/api/projects/status/github/0x90d/videoduplicatefinder?branch=master&svg=true)](https://ci.appveyor.com/project/0x90d/videoduplicatefinder/branch/master/artifacts) (You need to download FFmpeg and FFprobe yourself, see below!)

# Requirements

#### Windows user:
FFmpeg and FFprobe are already included except for AppVeyor builds. Otherwise get latest package from https://ffmpeg.zeranoe.com/builds/ and extract ffmpeg.exe and ffprobe into the same directory where VideoDuplicateFinderWindows.exe is placed in.

#### Linux user:
Install latest ffmpeg and ffprobe the usual way and verify PATH environment variable is set. Also make sure you got **libgdiplus** installed.

```
sudo apt-get update
sudo apt-get install ffmpeg
sudo apt-get install libgdiplus
```

# Screenshots
![windows](https://user-images.githubusercontent.com/46010672/50975469-97e5d900-14e5-11e9-9aba-5a843546ac2c.jpg)
![linux](https://user-images.githubusercontent.com/46010672/50975476-9e745080-14e5-11e9-8332-b0ac816458f4.jpg)


# License
Video Duplicate Finder is licensed under GPLv3  
Video Duplicate Finder uses ffmpeg / ffprobe (not included) which is licesed under LGPL 2.1 / GPL v2


# Compiling / Building

- You need the `dotnet` SDK, at least `3.x`, `5.x` is probably okay too
  - Daily .NET Core 3.x SDK builds https://github.com/dotnet/core-setup#daily-builds
- Linux:
  - Linux builds require the Avalonia NuGet package to provide support for GUI programming. `dotnet restore` should take care of this.

## Build Script

A bash script that builds every distribution, `build.sh` is provided. If your development machine is windows, you'll need to use Cygwin to run it.

If your development machine is *nix, you won't be able to target Windows.

## Docker

A dockerfile, `compose.yml` spec, & a sample `compose.override.yml` spec have been provided for the webapp.

Running `docker-compose up` will launch the webservice, listening on `localhost:5000`, as well as a seq logging server, running on `localhost:9080`


# Development

- Visual Studio 2019 is a very nice IDE, but not strictly necessary.

