---
layout: post
title: Deep Clustering Activation Maps for Emphysema Subtyping
categories: [Paper Published,Medical Imaging Analysis]
excerpt:  I propose a deep learning clustering method that exploits dense features from a segmentation network for emphysema subtyping from computed tomography (CT) scans. This approach provides model interpretability via dense clustering activation maps (dCAMs). On the evaluation dataset with 500 subjects, the method achieved a 43% unsupervised clustering accuracy, 0.54 in silhouette coefficient, and 0.55 in David-Bouldin scores.
---


## Table of Contents
**[Motivation](#motivation)**<br>
**[Method](#method)**<br>
**[Results](#results)**<br>
**[Cite](#cite)**<br>

 
### Motivation
This study proposes a deep learning-based clustering framework to find emphysema subtypes in a data-driven fashion. The existing approaches in this field are k-means based clustering methods that use hand-craft features, meaning that they are hardly reproducible and sensitive to changes. Furthermore, we address the issue of the lack of model interpretability in deep learning clustering methods by visualizing dense class activation maps as the regions reflect the clustering decisions.

### Method
The key innovation of this method is to use a deep clustering framework, which alternates between learning the clustering assignment and feature extraction by freezing parts of the network depending on the learning objective. Meanwhile, we use a segmentation network as the backbone to generate clustering activation maps in high-resolution, which improves the model interpretability. The following figure shows how to alternate between clustering and feature extraction in the deep clustering framework.
<table>
    <tr>
        <img alt="Qries" src="https://lh3.googleusercontent.com/V-EqOGoPWdUYWOOvlNOvCRtFg3mQyVydEESB34aVbfyxsCP5TQqNQo4JzCH66F66d8n1oO2h8LBWq9FlKVHcPUa3OxRJjrGOozRjb-qc--YdxzcHlwgOL_Ins2qj4AK3jW76G2v1pj_wIfUkK46E9m4dR2nfiEhC3rVaVBpJsxdljSj4X71lTLCfXo5AKBziWE-BfQ1HuxWnig7-7PheLJZUbaXo-bAzmRzDoPtFBDV3Wj47jP6oU9Yzjywp6KcThGgJRt9KJFxUg65m6ra8XH8koousfXr4qbw50wX-ruwzyI-soZPwC6-h9KR8Id0TYUhBmEANKjAIggv8smHf0Gql0G67fdhfHh4P4DVczrlVyv34WofAtAdTryoZWS2k-KQAtNqY9lnZyyCIDK5kPiMf7BlEPchLVZLPuElJXhLzAAA_FvkWcjrb4wA1VGXKoObAimeH8nJ9DEmKnbam3ZTjjmvZDV5xcmEh6RVXTORo8nO3lWez0Gyxfva-J4wv8NkqV_lbRhrTgcbDqExLiKAZPJFO53B9NpH_e2whgCioBhZDNxCzh1FHkelgthqCqvdJ7E31liHQvdtjCeuLLuqBk7az7QoSLzDziOGJ_IRh03xCc8ZzWncIyow4obkmR2Ew7YTNKxUOIrRiXj4eKvhOY226yAgi4tXlBhmgd8iBmlGcnfXxzpSZUHjg-1iyEnV5Ypr2fn4_NGaFkQOILaw=w772-h276-no?authuser=0" width=600 >
    </tr>
</table>

 please refer to the [published paper](https://arxiv.org/abs/2106.01351) for more details.
 
### Results
* We evaluated on 500 scans. The proposed model reached 43% unsupervised clustering accuracy, outperforming the baseline at 41%,. In terms of internal cluster measurement, we achieved 0.55 in DavidBouldin index and 0.54 in silhouette coefficient, showing a substantial improvement over the baseline.
 <table>
    <tr>
        <img alt="Qries" src="https://lh3.googleusercontent.com/O82RFhlA75D-maDU_Wii82QWZ4WdTrF_1LdDTJ7bJ27hEVWClcP_HRY62aRNlglr7V5ZUjNgiCKh13yYOOyXsa_AjeCQWcXxz4tqmzmyvxiRMbRyQC4saAwtriI7O-uBeGRds6h0dAB5yKQi29rp6CFf9bf_lgI5L1cfF8elyoGHd5yp8XKGA-fHuQlpldY96VKd5XhldJcrfgY0m3baPbkNY6fyIErwz27x1tnX_OSIujudPxsrxbkhy-AF87wSS2eFL-a_21MZ84-m_DCpNV5jrORk4zGt-Wiw2OpNsD-mvU862dM6eR6jRU0pZINj9KPd9yn80D6DJuFz2GAYEdBi00wCyc2athdsoeYubmLdiAG7AZeJmLC7qMuqKhS_3JDh3B4JOa3EcQx-UNtqmCbmbO2QD4yGKPR3Es-l8JuKQq_zX2WjPr8MO-jZB0rVpQV0qYqPHyWYZ2CWmOSUu8inxn54MY2-fgQjY6E-bf6rNGTzdrPq-LN_cDq2PIcRBkwEbeSD9xeNZ74d-Slrj3dNB_zDF-IMm1h7vFQP7FxJKT98omMeLBA48w5miL_CfuJYysxnmIm6ZBJL_LbcZ84fO87qm1RlvnXu6s9qedqYaE29oIP6EN2NRcAjCJvQh3Ql-5qWQlRQoUIIMfSu2EishiowxV9VFYlBYdcO9lFwQ3plJwMs8B90zU6uU4zrpyYPBdmNWi5GWiPgy_2nJBs=w1038-h649-no?authuser=0" width=600>
    </tr>
 </table>


### Cite
If you find this algorithm useful in your research, please consider citing:

	@article{xie2021dense,
	    author={Xie, Weiyi and Jacobs, Colin and van Ginneken, Bram},
	    title={Deep Clustering Activation Maps for Emphysema Subtyping},
	    journal={arXiv preprint arXiv:2106.01351},
	    year = {2021},  
	}

