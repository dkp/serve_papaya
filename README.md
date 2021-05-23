---
layout: default
---
# Brain Scans

An excellent source of technical information about MRI sequences is the [MR-TIP website](https://www.mr-tip.com/serv1.php).

##  Structural (Anatomical) Images
**This is a T1w image: [T1w Image](t1w.html)**
- You will usually acquire a T1-weighted structural (a.k.a anatomical) image.
It takes about 5 minutes and has voxels ~one-millimeter in each dimension (1 mm isotropic)
This is considered high resolution because it is much better than typical fMRI or DWI.

**This is a defaced T1w image: [Defaced T1w Image](t1w_defaced.html)**

- Defacing is done to protect the identity of the participant.
HIPAA requires that you deidentify MRI data. One part of this process is defacing
(removing identifying features).  This is not the same as brain extraction.


**This is a T2w image: [T2w Image](t2w.html)**

**This is a FLAIR image: [FLAIR Image](flair.html)**

## Standard Space Images
**This is an image in standard space: [MNI Image](mni.html)**

- To compare and analyze brain images from different individuals, the images must be
"warped" to a standard "space" (template). The most common standard spaces were developed
by the Montreal Neurological Institute (MNI). Because this image is in a standard space,
you can move the mouse to display which brain region the pointer is in (displayed at
the bottom of the viewer).


## 4D Image Sequences
**This is a DWI image: [DWI Image](dwi.html)**

- Diffusion images (a.k.a. DTI [Diffusion Tensor] or DWI [Diffusion Weighted] Images)
are used to examine the integrity of white matter. This one has 30 volumes,
each with a different gradient directions applied. It also includes two B0 (b-zero)
images, for a totoal of 32 volumes. B0 images have no gradients applied, They appear
as the first and last image in the sequence (and are much brighter than the images
with the gradients). This is probably the minimum you would want for research. 
If you double the number of directions, you'll also double the acquisition time! 
This sequence has 2 mm isotropic voxels and takes about 5 minutes to acquire. 
It was acquired with A-P (anterior to posterior) phase encoding, which is also pretty typical.  


**This is an fMRI image: [fMRI Image](fmri.html)**

- This resting state fMRI (functional magnetic resonance image). This one includes
177 volumes, repeated every 2 seconds (i.e., repetition time, TR, is 2 seconds). 
It takes about 6 minutes to acquire. Voxels are 2.5 x 2.5 x 3.5 mm, so they are
anisotropic (not the same in every dimension). It is often suggested that resting
state scans be longer, but it depends on whether your participants can hold still
and avoid going to sleep for a longer scan.

## Field Maps

- Field maps take about 1.5 minutes to acquire and are extremely useful for correcting
distortions in DTI or even fMRI sequences. A typical field map sequence on our Siemens
scanner includes two magnitude images and one phase image (like the lower one).
The voxels are 3 x 3 x 4 mm. Note: fmriprep will only find and use the field maps IF
there is an IntendedFor key and value in the accompanying JSON files for each fieldmap.
You can read more about the issue [here](https://github.com/nipreps/fmriprep/issues/2312).

**This is a Magnitude image: [Magnitude Image](magnitude.html)**

**This is a Phase image: [Phase Image](phasediff.html)**
