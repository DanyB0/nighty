[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)
# nighty
### nighty is a simple nightcore song maker (+ video)
## Installation
- #### clone the repo wherever you want
  ```
  git clone https://www.github.com/DanyB0/nighty
  ```
- #### install the requirements (you MUST have ffmpeg installed)
  ```
  pip install -r requirements.txt
  ```
- #### you're ready to go!
## Usage
- put in the "ingredients" folder one or more songs and one or more images
- `python main.py`
- in the "final" folder will be created your video
#### how to have the wavesound like in the example below
- create the nightcore video and copy-paste tis code in a terminal (change the name of your video)
```
ffmpeg -i <YOUR VIDEO NAME>.mp4 -filter_complex "[0:a]showwaves=s=cif:mode=line:colors=white,colorkey=0x000000:0.01:0.1,format=yuva420p[v];[0:v]scale=cif[bg];[bg][v]overlay[outv]" -map "[outv]" -map 0:a -c:v libx264 -c:a copy video-soundwave.mp4
```
## example
https://www.youtube.com/watch?v=CIRylCFM-28
## Team
This project is maintained by me.
[![DanyB0](https://avatars.githubusercontent.com/u/66164380?s=100)](https://github.com/DanyB0) |
--- |
[DanyB0](https://github.com/DanyB0) |
## License
[BSD 3-Clause License](./LICENSE)
