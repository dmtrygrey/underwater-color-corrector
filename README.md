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
