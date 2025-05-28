# ffmpegthumbnailer.yazi

An alternative, slightly modified [video](https://github.com/sxyazi/yazi/blob/main/yazi-plugin/preset/plugins/video.lua) plugin for [yazi](https://github.com/sxyazi/yazi) that uses [ffmpegthumbnailer](https://github.com/dirkvdb/ffmpegthumbnailer) instead of [ffmpeg](https://ffmpeg.org). Should be noticeably faster (does not require expensive video duration extraction).

## Requirements

- `ffmpegthumbnailer`

## Installation

```sh
ya pack -a 'ze0987/ffmpegthumbnailer'
```

## Usage

Add the following to your `yazi.toml`:

```toml
[plugin]
prepend_previewers = [
  { mime = "video/*", run = "ffmpegthumbnailer" },
]

prepend_preloaders = [
  { mime = "video/*", run = "ffmpegthumbnailer" },
]
```
Don't forget to clear the Yazi cache before first use:
```sh
yazi --clear-cache
```
