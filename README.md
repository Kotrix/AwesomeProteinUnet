# AwesomeProteinUnet
The summary of all resources related to the ProteinUnet architecture


## ProteinUnet


### Abstract

Predicting protein function and structure from sequence remains an unsolved problem in bioinformatics. The best performing methods rely heavily on evolutionary information from Multiple Sequence Alignments, which means their accuracy deteriorates for sequences with a few homologs, and given the increasing sequence database sizes requires long computation times. Here, a single-sequence-based prediction method is presented, called ProteinUnet, leveraging a U-Net convolutional network architecture. It is compared to SPIDER3-Single model, based on LSTM-BRNNs architecture. Both methods achieve similar results for prediction of secondary structures (both 3- and 8-state), half-sphere exposure, and contact number, but ProteinUnet has two times fewer parameters, 17 times shorter inference time, and can be trained 11 times faster. Moreover, ProteinUnet tends to be better for short sequences and residues with a low number of local contacts. Additionally, the method of loss weighting is presented as an effective way of increasing accuracy for rare secondary structures.

### Code

- CodeOcean inference code and reproducible capsule: https://codeocean.com/capsule/2521196

### Citation

> Krzysztof Kotowski, Tomasz Smolarczyk, Irena Roterman-Konieczna, Bogdan Ruszczak, and Katarzyna Stapor.
> ProteinUnet - An efficient alternative to SPIDER3-single for sequence-based prediction of protein secondary structures. Journal of Computational Chemistry, 2021.
> doi:[10.1002/jcc.26432](https://doi.org/10.1002/jcc.26432)

```bibtex
@article{kotowski_proteinunetefficient_2021,
	title = {{ProteinUnet}—{An} efficient alternative to {SPIDER3}-single for sequence-based prediction of protein secondary structures},
	volume = {42},
	issn = {1096-987X},
	doi = {10.1002/jcc.26432},
	number = {1},
	journal = {Journal of Computational Chemistry},
	author = {Kotowski, Krzysztof and Smolarczyk, Tomasz and Roterman-Konieczna, Irena and Stapor, Katarzyna},
	year = {2021},
	pages = {50--59},
}
```

## ProteinUnet2


### Abstract

We present a lightweight deep network ProteinUnet2 for SS prediction which is based on U-Net convolutional architecture and evolutionary-based input features (from PSSM and HHblits) as well as SPOT-Contact features. Through an extensive evaluation study, we report the performance of ProteinUnet2 in comparison with top SS prediction methods based on evolutionary information (SAINT and SPOT-1D). We also propose a new statistical methodology for prediction performance assessment based on the significance from Fisher–Pitman permutation tests accompanied by practical significance measured by Cohen’s effect size. Our results suggest that ProteinUnet2 architecture has much shorter training and inference times while maintaining results similar to SAINT and SPOT-1D predictors. Taking into account the relatively long times of calculating evolutionarybased features (from PSSM in particular), it would be worth conducting the predictive ability tests on embeddings as input features in the future. We strongly believe that our proposed here statistical methodology for the evaluation of SS prediction results will be adopted and used (and even expanded) by the research community.

### Code
- CodeOcean inference code and reproducible capsule: codeocean.com/capsule/0425426

### Citation

> Katarzyna Stapor, Krzysztof Kotowski, Tomasz Smolarczyk, and Irena Roterman.
> Lightweight ProteinUnet2 network for protein secondary structure prediction: a step towards proper evaluation. BMC Bioinformatics, 2022.
> doi:[10.1186/s12859-022-04623-z](https://doi.org/10.1186/s12859-022-04623-z)

```bibtex
@article{stapor_lightweight_2022,
	title = {Lightweight {ProteinUnet2} network for protein secondary structure prediction: a step towards proper evaluation},
	volume = {23},
	issn = {1471-2105},
	doi = {10.1186/s12859-022-04623-z},
	journal = {BMC Bioinformatics},
	author = {Stapor, Katarzyna and Kotowski, Krzysztof and Smolarczyk, Tomasz and Roterman, Irena},
	year = {2022},
	pages = {100},
}
```

## ProteinUnetLM

### Abstract

The protein secondary structure (SS) prediction plays an important role in the characterization of general protein structure and function. In recent years, a new generation of algorithms for SS prediction based on embeddings from protein lan-guage models (pLMs) is emerging. These algorithms reach state-of-the-art accuracy without the need for time-consuming multiple sequence alignment (MSA) calculations. LSTM-based SPOT-1D-LM and NetSurfP-3.0 are the latest examples of such predictors. We present the ProteinUnetLM model using a convolutional Attention U-Net architecture that provides pre-diction quality and inference times at least as good as the best LSTM-based models for 8-class SS prediction (SS8). Addi-tionally, we address the issue of the heavily imbalanced nature of the SS8 problem by extending the loss function with the Matthews correlation coefficient (MCC), and by proper assessment using previously introduced adjusted geometric mean metric (AGM). ProteinUnetLM achieved better AGM and sequence overlap score (SOV) than LSTM-based predictors, especially for the rare structures 310-helix (G), beta-bridge (B), and high curvature loop (S). It is also competitive on chal-lenging datasets without homologs, free-modeling targets, and chameleon sequences. Moreover, ProteinUnetLM outper-formed its previous MSA-based version ProteinUnet2, and provided better AGM than AlphaFold2 for 1/3 of proteins from the CASP14 dataset, proving its potential for making a significant step forward in the domain. 

### Code
- GitHub: https://github.com/Kotrix/ProteinUnetLM
- CodeOcean inference code and reproducible capsule: https://codeocean.com/capsule/4357959
- Biolib prediction server: https://biolib.com/SUT/ProteinUnetLM
- Training notebook: https://colab.research.google.com/drive/1Onh6xlg-a-_QDy2EL_t9XmKa8T3VLVEv

### Citation

> Krzysztof Kotowski, Piotr Fabian, Irena Roterman, and Katarzyna Stapor.
> Convolutional ProteinUnetLM competitive with long short-term memory-based protein secondary structure predictors. Proteins: Structure, Function, and Bioinformatics, 2022.
> doi:[10.1002/prot.26452](https://doi.org/10.1002/prot.26452)

```bibtex
@article{kotowski_convolutional_2022,
	title = {Convolutional {ProteinUnetLM} competitive with long short-term memory-based protein secondary structure predictors},
	issn = {1097-0134},
	doi = {10.1002/prot.26452},
	journal = {Proteins: Structure, Function, and Bioinformatics},
	author = {Kotowski, Krzysztof and Fabian, Piotr and Roterman, Irena and Stapor, Katarzyna},
	year = {2022},
}
}
```

## DisorderUnetLM

CAID-3 challenge https://caid.idpcentral.org/challenge/results
- 7th place (3rd tier) for Disorder-NOX dataset 
- 4th place (2nd tier) for Linker dataset


### Abstract

The prediction of intrinsic disorder regions has significant implications for understanding protein functions and dynamics. It can help to discover novel protein-protein interactions essential for designing new drugs and enzymes. Recently, a new genera-tion of predictors based on protein language models (pLMs) is emerging. These algorithms reach state-of-the-art accuracy with-out calculating time-consuming multiple sequence alignments (MSAs). This article introduces the new DisorderUnetLM disor-der predictor, which builds upon the idea of ProteinUnet. It uses the Attention U-Net convolutional network and incorporates features from the ProtTrans pLM. DisorderUnetLM achieves top results in the direct comparison with recent predictors exploit-ing MSAs and pLMs. Moreover, among 43 predictors on the latest CAID-2 benchmark, it ranks 1st for the NOX subset in terms of the ROC-AUC metric (0.844) and 2nd for the AP metric (0.596). For the CAID-2 PDB subset, it ranks in the top 10 (ROC-AUC of 0.924 and AP of 0.862). 

### Code

- CodeOcean inference code and reproducible capsule: https://codeocean.com/capsule/0867702

### Citation

> Krzysztof Kotowski, Irena Roterman, and Katarzyna Stapor.
> DisorderUnetLM: Validating ProteinUnet for efficient protein intrinsic disorder prediction. Computers in Biology and Medicine, 2025.
> doi:[10.1016/j.compbiomed.2024.109586](https://doi.org/10.1016/j.compbiomed.2024.109586)

```bibtex
@article{kotowski_disorderunetlm_2025,
	title = {{DisorderUnetLM}: {Validating} {ProteinUnet} for efficient protein intrinsic disorder prediction},
	volume = {185},
	issn = {1097-0134},
	doi = {10.1016/j.compbiomed.2024.109586},
	journal = {Computers in Biology and Medicine},
	author = {Kotowski, Krzysztof and Roterman, Irena and Stapor, Katarzyna},
	year = {2025},
	pages = {109586},
}
}
```
