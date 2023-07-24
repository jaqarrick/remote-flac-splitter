# Flac splitter
Use this utility if you have a _remote_ `.flac` file you would like to split up into individual tracks. This command will:
1. Download the flac directory
2. Split the files on your local machine
3. Replace the remote directory and unsplit `.flac` files with individual tracks.
4. Optional: keep a copy of the original `.flac` file locally.

_Why perform the splitting locally and not on the server itself?_: If you don't have sudo access to a server where your files live it can be difficult to install necessary binaries for flac splitting.

## Prerequisites
- Install the [unflac](https://git.sr.ht/%7Eft/unflac) binary. _Note: to install you'll also need [Go](https://go.dev/) and [ffmpeg](https://ffmpeg.org/)_.
- SSH credentials for the server storing the remote directory
- **The `.flac` file must be contained inside a directory that also includes a `.cue` file.**

## Installation
🚧 Todo 🚧

## Usage

```
remote_flac_split source_dir [-o target_dir]```
```
Examples:

```
$ remote_flac_split "/some/path/to/a/directory"
```
Files will download to current directory unless specified otherwise with `-o`:
```
$ remote_flac_split /some/path/to/a/directory -o ~/Music/album
```
