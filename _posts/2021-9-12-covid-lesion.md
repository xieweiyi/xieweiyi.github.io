---
layout: post
title:  Dense Regression Activation Maps For Lesion Segmentation in CT scans of COVID-19 patients
categories: [Paper Published,Medical Imaging Analysis]
excerpt:  I propose a weakly-supervised segmentation method based on dense regression activation maps (dRAMs). Most weakly-supervised segmentation approaches exploit class activation maps (CAMs) to localize objects. However, because CAMs were trained for classification, they do not align precisely with the object segmentations. Instead, my method produce high-resolution activation maps using dense features from a segmentation network that was trained to estimate a per-lobe lesion percentage. In this way, the network can exploit knowledge regarding the required lesion volume. We evaluated our algorithm on 90 subjects. Results show our method achieved 70.2% Dice coefficient, substantially outperforming the CAM-based baseline at 48.6%.
---


## Table of Contents
**[Motivation](#motivation)**<br>
**[Method](#method)**<br>
**[Results](#results)**<br>
**[Cite](#cite)**<br>

 
### Motivation
Most weakly-supervised segmentation approaches exploit class activation maps (CAMs) to localize objects. However, because CAMs were trained for classification, they do not align precisely with the object segmentations. Instead, we produce high-resolution activation maps using dense features from a segmentation network that was trained to estimate a per-lobe lesion percentage. In this way, the network can exploit knowledge regarding the required lesion volume.

### Method
The key innovation of this method is to generate activation maps by regression training instead of standard classification training. In this way, we can let the network to measure certain properties of the object of interest, such as the volume size and roundness, providing richer semantic information than the categorical labels. Meanwhile I design an attention neural network module to replace standard denseCRF based refinement steps such as refinement of activation maps can be optimized with the main network. This attention neural network module works very similar to random-walk or seeded regional growth based on convolution features. The following figure shows the overview of this method.   
 <table>
    <tr>
        <img alt="Qries" src="https://lh3.googleusercontent.com/naG33aD95n3ek0a1jeHLbTAKMvbYGeelovpOJGzpuR_aTH0qp9DsUKgT3vRuSFqXht-PpjupUOrZIRPr2YigxLC5cVbAkn6KzOmNRyh-rq1Ai3dhjqvb5HfkksJiSYuFdhSF4CHnbzNkgTPu8_yxxs5N7qS3QexSzc2boz9QiD3JsWAGvUp5zwIYm_rQcTzsyatpSpd9xrhnxhLi6vQfVZHKNhk5b99BSxzuNyy6zpH-xifHK65eZjW0h5dwRmzWZj6WDcECw_epLAB9m4vLW0qGTy0oe4V44PkiFvIbHK4rWhsyG7YTdqlZ3LcMsHwHGbs-hG0RxjdNRXvFo3xDy83y7z08J1nEdDXEY95KCYYwoOQP7xXvqt_3yfe8PIPsxckaADcqvn_HDsWtJo503th33QAXpey9Y4udO_paZlmCCjEtWsTVXPKVPJOEYFRmIj9ZgvBeEv3_z4asRayavJenXGxECvtADTKlYmDJ9tVj6OGc-2VWWvJaxtfC2GAxAwT4WLDnVh76BX5ZQflx4SUft7OovRGDAbt8bI4wdnGnUggRMYzMioBG2z62mWKevXaJSVlSKAwlWDS5ThMI1t8W2gGfaOkzr3kcS3ZrL9Je67VIgwpSVXTEA7_2UdHUgMUZ0YrqCGe-54gCIGtYGpVexhyc-1hq7SfVeEUcG3oTAVUa8awKqId7IDx-2LmVnrNyULrJJA6Y42G801MeGuc=w1231-h519-no?authuser=0" >
    </tr>
</table>
 please refer to the [published paper](https://arxiv.org/abs/2105.11748) for more details.
 
### Results
* We achieved overall Dice at 70.24, where the fully-supervised nnU-Net reaches 77.09. The performance gap between weakl-supervised approach and fully-supervised method is aligned with results on benchmark datasets (e.g., PASCAL VOC2012).

* This method is robustness against various subtypes of covid-19 lesions, shown as the following figure.
   <table>
    <tr>
        <img alt="Qries" src="https://lh3.googleusercontent.com/0YK12LgJuQVXFU8vOhBt-JaT1gj34gDGGk20nbgrZOJdFeVWa_Eb3u3Q-wlGBv7ON_fp4dPMmgJAloV41wlW0f-dzGmSWWOQAmQlIjyffMnuB0jeapLiQaM3lSZKMypRjONeQ041rduXdL-cDEd9VfC7MI9ZcibjbPZiKzPmrN8Q-q3uuTp-z9WHm4Z27-zwkP6sGyQ4mFTMCIG96kh88I3TwdDKud7TwMAINFY95FYaqtQG_GHkXOHL3etvBpPSLq6HYkguHkMqpMUDpl9F0cnBapVhbJp3nxXtWZ_E_ogPBRcyl2DjfeDCgISNMUfO74FTmKFKxbDsXVmbH-sl3_xWlMSYY6uvQ6MJ9FUMJlz0EQ6-cmdDQz2ruCvhDlDT7cDANF0PJAEMuyep2yQ-2QnO7QSXjO0Wp6Z3qsZe7hUEGSLnzEfQrzzMlwy3_317TqqA6u6Q9-NuL3E_4J8j5pptA2T8_Zmwj1gzM7d8PwjxRmVdNrjQxleQDPckji1zTmGBEvLxCdRhC-F8a1V_yW4XxzHtoQpObZZu7QPGAb8qBBM7s3TDcVZtMgD5r7fb4xeyd3q6_JQ3980SVNloKg0zEaN4Se1JQ3MJqHH-8H7DihIrtC5uGisE4uE-UZ1ADCWkYZe9FX0b9ASynAJ72_tSsfaZWmxkPKTxx4lNSfZgt6jbk7Ax2bKeVFn08OwgAEFNu2TqJ5fOAWT_zIcivtQ=w766-h739-no?authuser=0" width=500 >
    </tr>
  </table>

### Cite
If you find this algorithm useful in your research, please consider citing:

	@article{xie2021dense,
	    author={Xie, Weiyi and Jacobs, Colin and Charbonnier, Jean-Paul and van Ginneken, Bram},
	    title={Dense Regression Activation Maps For Lesion Segmentation in {CT} scans of {COVID}-19 patients},
	    journal={arXiv preprint arXiv:2105.11748},
	    year = {2021},  
	}

