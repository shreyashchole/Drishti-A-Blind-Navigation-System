# Drishti: A Blind Navigation System

A Smart Blind Baseline System helps **blind people to sense their environment** by estimating the *depth* in a real-time image and them for the next step direction (**2100 milli-radian  coverage in 3-5  splits**). 

## Requirements
* This code is tested with `Tensorflow 2.3`,  on a machine with a *NVIDIA GTX 1650ti* and 8GB+ RAM running on Windows 10 or Ubuntu 16.
* Other packages needed `Numpy`, `Open-cv`, `Matplotlib`, `PIL`.

## Evaluation

#### 1. Images

* Clone the Repository. Put the images (.jpg) in `images` folder in the directory.
* Run

        python depth.py -m nyu -i images -s 5
        
* Arguments
        
        -m: Model Name (1. {nyu: NYU Depth V2 }, 2. {kitti: KITTI})
        -i: Image folder to be evaluated ( default folder: images)
        -s: Final direction guide (3, 5)
            5- ['ext-left', 'left', 'forward', 'right', 'ext-right']
            3- ['left', 'forward', 'right']
            
* Results

<img src="results/result2.gif" height="300">


#### 1. Videos

* Clone the Repository. Put the video in `videos` folder in the directory.
* Run

        python cam_depth.py -m nyu -v video.mp4 -s 5
        
* Arguments
        
        -m: Model Name (1. {nyu: NYU Depth V2 }, {kitti: KITTI})
        -i: video-file name under 'videos' folder to be evaluated (default folder: video.mp4)
        -s: Final direction guide (3, 5)
            ['ext-left', 'left', 'forward', 'right', 'ext-right']
            
* Results

<img src="results/result.gif">
        
        
