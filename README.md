<h1 align='center' style="text-align:center; font-weight:bold; font-size:2.0em;letter-spacing:2.0px;"> EQGAT-diff: Navigating the Design Space of Equivariant Diffusion-Based Generative Models for De Novo 3D Molecule Generation </h1>

<p align='center' style="text-align:center;font-size:1.25em;">
    <a >Tuan Le<sup>1*</sup></a>&nbsp;,&nbsp;
    <a >Julian Cremer<sup>1*</sup></a>&nbsp;,&nbsp;
    <a >Djork-Arné Clevert<sup>1</sup></a>&nbsp;,&nbsp;
    <a >Kristof T. Schütt<sup>1</sup></a>&nbsp;,&nbsp;
<b>
<sup>*</sup>Equal contribution&nbsp;&nbsp;&nbsp;
<sup>1</sup>Pfizer Research & Development&nbsp;&nbsp;&nbsp;
</p>


<p align='center';>
<b>
<em>ICLR, 2024</em> <br>
</b>
</p>
<p align='center' style="text-align:center;font-size:2.5 em;">
<b>
    <a href="https://openreview.net/forum?id=kzGuiRXZrQ" target="_blank" style="text-decoration: none;">[Paper]</a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</b>
</p>


This is the official repository for EQGAT-diff - a model for 3D molecule generation  via equivariant (continuous and discrete) denoising diffusion. The code is inside eqgat_diff and is work in progress. If you have any questions, feel free to reach out to us: [julian.cremer@pfizer.com](julian.cremer@pfizer.com), [tuan.le@pfizer.com](tuan.le@pfizer.com).


Find the inference subdirectory: ./eqgat-diff/tree/main/inference
Find the link to download the model weights for the QM9 and Geom-Drugs models here: https://drive.google.com/drive/folders/1_qqhKRU4GI43uSMFB0cMgreLxubZGYWZ?usp=share_link
 
For QM9, the provided checkpoint is the model after 300 epochs of training of EQGAT^{x0}_{disc} as in Table 2,  while for GEOM-Drugs, I have attached the checkpoint to the model EQGAT^{x0}_{disc}  that was further trained as described in Table 3. 
 
Please place the model weights into the subfolders ./eqgat-diff/tree/main/weights, like so:

weights:
    geom:
        best_mol_stab.ckpt
    qm9:
        best_mol_stab.ckpt
 
We provide two notebooks to play around with the model (e.g. ./inference/sampling_geom.ipynb)
Make sure to extract the two data folders here: ./data


</details>
Below, we show some sampling trajectories from our models. The corresponding .gif files can be found in the `assets/` directory.


### Unconditional Sampling Trajectory

<img src="https://github.com/tuanle618/eqgat-diff/blob/main/assets/unconditional-sampling-trajectory.gif" width="400" height="300"/>


### Conditional Sampling Trajectory on maximized polarizability


<img src="https://github.com/tuanle618/eqgat-diff/blob/main/assets/conditional-sampling-maximized-polarizability.gif" width="400" height="300"/>

### Conditional Sampling Trajectory on minimized polarizability

<img src="https://github.com/tuanle618/eqgat-diff/blob/main/assets/conditional-sampling-minimized-polarizability.gif" width="400" height="300"/>



### Conditional Sampling Trajectory on a fixed protein pocket

<img src="https://github.com/tuanle618/eqgat-diff/blob/main/assets/conditional-ligand-pocket-sampling-trajectory.gif" width="400" height="300"/>



## Acknowledgement
This study was partially funded by the European Union’s Horizon 2020 research and innovation programme under the Marie Skłodowska-Curie Actions grant agreement “Advanced machine learning for Innovative Drug Discovery (AIDD)” No. 956832.