## Segmentation of fluid on OCT

Presence of fluid, as visualised by optical coherence tomography (OCT) is an important indication for treatment for several retinal diseases.   
Manual segmentation is subjective, tedious and time-consuming. 
Therefore, we whish to automate this process.

### Dataset
In the folder `sample`, you will find three subfolders: `oct`, `irf`  and `srf`

The folder `oct` contains grayscale OCT images. The irf and srf folder contain manually segmentation masks for intraretinal fluid and subretinal fluid respectively.
OCT images can be linked to their respective segmentation masks based on their filenames.

Example an OCT-scan with IRF (left-to-right: OCT, IRF and SRF):

<img src="sample/oct/16.png" style="display:inline-block; width: 200px;"/> <img src="sample/irf/16.png" style="display:inline-block; width: 200px;"/> <img src="sample/srf/16.png" style="display:inline-block; width: 200px;"/>

Example of an OCT-scan with SRF (left-to-right: OCT, IRF and SRF):

<img src="sample/oct/30.png" style="display:inline-block; width: 200px;"/> <img src="sample/irf/30.png" style="display:inline-block; width: 200px;"/> <img src="sample/srf/30.png" style="display:inline-block; width: 200px;"/>

Example of an OCT-scan with both IRF and SRF (left-to-right: OCT, IRF and SRF):

<img src="sample/oct/23.png" style="display:inline-block; width: 200px;"/> <img src="sample/irf/23.png" style="display:inline-block; width: 200px;"/> <img src="sample/srf/23.png" style="display:inline-block; width: 200px;"/>

Note that some scans have neither IRF nor SRF.

## Tasks

You task is to implement a segmentation model that takes as input and OCT-scan and produces binary segmentation masks representing IRF and SRF.  
We do not expect you to deliver a perfectly trained model, but do like to know your thoughts on particular implementation details that may require particular attention in this pipeline.

If you can implement parts of the pipeline that is great, otherwise please specify what functionality (input and expected output) is required at each step in pseudocode.

### 1) Data loading and preprocessing
Load the images into memory and prepare them for training the model.

- What input size do you use?
- How would you normalize the data?
- Which image transformations do you apply?

### 2) Model definition and initialization

Define a model that is able to take in an OCT-scan and produces two segmentation images: one representing IRF, and one representing SRF.

- What network architecture do you use? 
- Specify the exact input and output shapes and datatypes of the model

### 3) Training, validation and experimentation

How would you set up you experiments?

- What loss function do you use?
- Which validation metrics are useful here?
- Which (hyper)parameters should be tuned?
