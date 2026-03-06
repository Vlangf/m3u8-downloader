# m3u8_downloader

Simple Python tool to download M3U8/HLS streams and convert them to MP4.

## Features

- Parses master M3U8 playlists with multiple resolutions
- Lets you choose the desired resolution interactively
- Downloads and merges TS segments into a single file
- Converts to MP4 using ffmpeg
- Can also be used as a library in your own code

## Requirements

- Python 3.6+
- [ffmpeg](https://ffmpeg.org/) installed and available in PATH
- `requests` library

## Installation

```bash
pip install requests
```

## Usage

### CLI

```bash
python m3u8_downloader.py
```

You will be prompted to enter the M3U8 URL and choose a resolution if multiple are available.

### As a library

```python
from m3u8_downloader import M3u8Downloader

downloader = M3u8Downloader("https://example.com/playlist.m3u8")
downloader.from_m3u8_to_mp4(output_file_name="video")
```

#### Parameters

- `resolution` — specify a resolution string (e.g. `"1920x1080"`) to skip interactive selection
- `output_file_name` — set the output MP4 filename (without extension)

## License

MIT
