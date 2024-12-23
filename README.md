**LSTID forecasting**: LSTIDs Forecasting with the Temporal Fusion Transformer
========


**What it is**. This code utilizes a Temporal Fusion Transformer (TFT) to predict LSTIDs. The model incorporates features such as the auroral electrojet indices IL and IU provided by the FMI IMAGE network and the Gradient GNSS TEC Activity Index provided by DLR. The labels are the Spectral Energy Contribution (Spcont) for detected LSTIDs over Digisonde stations (in this case data from the Juliusruh Digisonde are used) calculated with the HF Interferometry method.

**About the code**. 

# Installation 
To install required python packages you should use the following command
```
pip install -r requirements.txt
```

# Models
We provide a forecasting model for each Digisonde station, i.e., Sopron, Juliusruh, Durbes, Ebro, trained over different time periods. All models are accessible through a corresponding notebook file that is named after the training and validation period of the model.

# Notebooks

Notebooks are presented to load the TFT forecasting models. Available models per station are
1. Dourbes
   - Training period 2022/01/01 - 2023/06/30. Use notebook here.
   - Training period 2022/01/01 - 2024/07/24. Use notebook here.
3. Juliusruh
   - Training period 2022/01/01 - 2023/06/30. Use notebook here.
5. Sopron
   - Training period 2022/01/01 - 2023/06/30. Use notebook here.
   - Training period 2022/01/01 - 2023/06/30. Use notebook here.
7. Ebro
   - Training period 2022/01/01 - 2023/06/30. Use notebook [here](notebooks/EB040/EB040_TFTmodel_20220101_20230630.ipynb).

# Output
The output of each model is the forecasted prediction of the model, given a horecast horizon interval of 5 min and a threshold of .7. Please read our paper for further information. The predicted output is presented in a figure containing both input drivers and predicted LSTIDs.

![figure]([http://url/to/img.png](https://github.com/themelis/LSTIDs_forecasting/blob/main/images/output_sample.png))

## Citation
If you use our TFT classifier for LSTID forecasting in your work, please use the following BibTeX entries:

<details>
<summary> bibtex </summary>

```latex
@misc{bel2024,
      title={Short-term forecast for the occurrence of Large Scale Travelling Ionospheric Disturbances at European middle latitudes using Neural Networks.},
      author={Themelis, K., Belehaki, A., Koutroumbas, K., Segarra, A., de Paula, V., Navas-Portella, V., & Altadill, D. },
      year={2024},
      doi={https://doi.org/10.5281/zenodo.14537425}
}


```
</details>

# License
LSTIDs Forecasting with the Temporal Fusion Transforme © 2024 by Konstantinos Themelis is licensed under Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International.  Please see the [LICENSE](LICENSE) file for more information.
