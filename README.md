# C3D

Modified version of [facebook/C3D](https://github.com/facebook/C3D)

## Setup
- Install nvidia-docker
- `git clone git@github.com:gursimar/C3D.git`
- `sudo nvidia-docker run -ti -v "$PWD/C3D/":/workspace/C3D gursimar/c3d-feature_extraction:latest` [download docker image]
- `cd C3D/C3D-v1.0/`
- `make all -j 8` [build caffe]

## Test feature extraction
- `cd examples/c3d_feature_extraction/`
- `wget https://www.dropbox.com/s/vr8ckp0pxgbldhs/conv3d_deepnetA_sport1m_iter_1900000?dl=0` [download sports1m model]
- `sh c3d_sport1m_feature_extraction_frm.sh`
- If out of memory, refer this [link](https://docs.google.com/document/d/1-QqZ3JHd76JfimY4QKqOojcEaf5g3JS0lNh-FHTxLag/edit)


## Running

## Changes
- Modified Makefile and Makefile.config to fix errors while building caffe.
- Added python scripts to extract features from the TGIF-QA dataset (frames).
