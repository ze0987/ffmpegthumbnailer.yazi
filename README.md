# ffmpegthumbnailer.yazi

An alternative, slightly modified [video](https://github.com/sxyazi/yazi/blob/main/yazi-plugin/preset/plugins/video.lua) plugin for [yazi](https://github.com/sxyazi/yazi) that uses [ffmpegthumbnailer](https://github.com/dirkvdb/ffmpegthumbnailer) instead of [ffmpeg](https://ffmpeg.org). Supports embedded images and should be noticeably faster (does not require expensive video duration extraction).

### Before
![before](https://github.com/user-attachments/assets/5ee2258e-6029-4ce1-96df-64a94eb4dd05) <sub><sup>Video used for the screenshot: [A Better Terminal File Manager](https://www.youtube.com/watch?v=l44HjrTQHGc) by The Linux Cast, CC BY 3.0 </sub></sup>
### After
![after](https://github.com/user-attachments/assets/c17838fd-0163-4b14-9c52-e346f825a063) <sub><sup>Video used for the screenshot: [A Better Terminal File Manager](https://www.youtube.com/watch?v=l44HjrTQHGc) by The Linux Cast, CC BY 3.0 </sub></sup>


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
