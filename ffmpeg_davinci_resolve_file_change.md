# How to convert media file to edit in davinci resolve

```
ffmpeg -i "file_i_want_edit.mp4" -c:v dnxhd -profile:v dnxhr_hq -pix_fmt yuv422p -c:a pcm_s16le file_i_want_edit.mov
```
