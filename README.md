## Dive and underwater image and video color correction with audio

**Sample images**

![Example](./examples/example.jpg)

**Sample video**

[![Video](https://img.youtube.com/vi/NEpl41-LMBs/0.jpg)](https://www.youtube.com/watch?v=NEpl41-LMBs)


### Setup
```
$ sudo apt install ffmpeg
$ sudo apt install pipx
$ python3 -m venv ccolor-venv
$ ./ccolor-venv/bin/pip3 install opencv-python numpy
```

### For images
```
$ ./ccolor-venv/bin/python3 correct.py image /my/raw.png /my/corrected.png
```

### For videos
```
$ ./ccolor-venv/bin/python3 correct.py video /my/raw.mp4 /my/corrected.mp4
```
Parallel:
```
parallel /home/bit/dev/underwater-color-corrector/ccolor-venv/bin/python3 correct.py video {} {.}-cor.mp4 ::: ~/path/to/vids/*.MP4
```

### TODO
- Remove output name, instead original name will be used with prefix
- Add audio merge as default with no param
- Copy video processed before merge into /tmp
- Move original video in ./bkp