---
layout: post
title:  Pulmonary Nodule Detection in Chest CT images
categories: [Medical Imaging Analysis]
excerpt: I developed algorithms to automatically detect pulmonary nodules in Chest CT and assess of the malignancy risk of found nodules. My method currently ranks the 2nd out of 1000+ teams worldwide in <a href="https://luna16.grand-challenge.org/Results/">Luna16 Grand-challenge</a>.
---

<table>
    <tr>
        <img alt="Qries" src="https://lh3.googleusercontent.com/LNT1EDzcsM2VLCDwyZHqM2vdntYVeqd8x0vzYrdX--pu66Z-mSIGnFJ9ZX7UJsOllXgRa7p5PTDWRGKziFPfJdoSdls1kUm-T1LnpAIkKgDVsUpYIdhBQgdG28nONvelPV1TbKlf4xKm7c1WSwu4xrhihQQPOYvygfKuX6UF6IBhqpDQRFJtIhIBPPg9qB_wHQBZltxiyTsbzdD6NRCz9PUNmts0fjIAXZBQjgv1rLekKDV5qdazuzzStUR3hofN3iJd4zSt-RGhjXndoOU_cCodNPUuGXJqZpc2jXeu1VQvNgv02kJq6Gok86JP9s7ej6D3dN0-Xe_HkEB1eVGG6upKcALrzgfZE6NEpThCKg6_6FzG1CT8RU7aK1_i7X8ZYYcIowHoAaiPgKrVTpfgthZS6nxcMySQTJhw8x2CfmQ3Eewa_rMKgDHGo7RU2H_9N_2uspcZuglVrkKfX_BKx8DomlvLirl1UDHx7Dq4c_gBLG13gg4uwczUSRtYC9QcfIZaJqiAfVZhawIiLBM5pWTzR_S_YGpkwe5gJ6Ot1h6Krz-8DHjqkOV9HnQ-OhzH44lAUugf9RwRvE-od8nFGxrivOlzha8jDgrQuFXw8GCTybZ3WUTkruajmpd3sjLpu0ebR0yf8dZGCtNkVhsfGel_yYI6YWdV6TBKOjP5_8p9CnD4f45v-22EQPi6D82yqelqqaFyr1S9Myu7aIoy210=w1766-h1091-no?authuser=0" >
    </tr>
</table>

## Table of Contents
**[Motivation](#motivation)**<br>
**[Method](#method)**<br>
**[Results](#results)**<br>


### Motivation
Pulmonary Nodule detection in CT imaging is an essential, yet very challenging task due to the wide variability of shape, textual and scale of pulmonary nodules. An automatic nodule detection system could facilitate large-scale lung screening trials as well as reduce the workload of radiological readings.

### Method
We propose a two-stage nodule detection framework that detects nodule candidate with convolution neural networks trained separately on 2d axial slices and 3d CT volume, followed by a deep residual 3d neural network to reduce false alarms. 


### Results
The proposed framework shows the superior performance on LUNA16 dataset, yielding the final 0.9499 free receive operating characteristic score. 