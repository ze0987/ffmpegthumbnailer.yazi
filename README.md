# ffmpegthumbnailer.yazi

An alternative video plugin for [yazi](https://github.com/sxyazi/yazi) that uses [ffmpegthumbnailer](https://github.com/dirkvdb/ffmpegthumbnailer) instead of [ffmpeg](https://ffmpeg.org). Supports embedded images, should be noticeably faster (does not require expensive video duration extraction) and saves some RAM/disk space (generates smaller thumbnails).
## Requirements

- `ffmpegthumbnailer`

## Installation

```sh
ya pack -a 'ze0987/ffmpegthumbnailer'
```

## Usage

Add this to your `yazi.toml`:

```toml
[plugin]
prepend_previewers = [
  { mime = "video/*", run = "ffmpegthumbnailer" },
]

prepend_preloaders = [
  { mime = "video/*", run = "ffmpegthumbnailer" },
]
```
