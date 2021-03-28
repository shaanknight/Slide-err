# Slide-err
These days, the demand for online lectures is increasing. For better visual experience,
along with the video of the lecture, soft copy of the slides is also being embedded into the
video. But most of the universities are manually matching slides from the video to the soft
copy which is a laborious task. 

So the problem statement is to automate this slide matching
process.

So to be more precise, given a set of noisy slide images extracted from the video and
a set of slides from the original ppt, we build a mapping for each of the sampled
noisy slides with the corresponding original slide.

For example in the dataset given, consider the slides in any of the folders. You will see
4-5 frames sampled from the lecture for which the corresponding ground truth slide is ppt.jpg.

Also note that the sampled frames are almost aligned with the corresponding ground truth
slide using homography.

The details of the 2 techniques used are mentioned in the pdf Report.pdf .

It is a simple yet effective way to accomplish the task . 

Accuracy : 94.9% against the dataset found here :
https://drive.google.com/open?id=1J84AcNchprI0DndeaTVFSUZWF2lMo5uu .

### Run Instructions 
```sh
python3 main.py <path/to/slides/directory> <path/to/frames/directory>
```

The script outputs a single file output.txt which should be a list of frames
with their corresponding predicted slide name separated by a single space.
