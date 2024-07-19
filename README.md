# ML Papers Checklist

At npj Computational Materials we are striving to set the highest standards for all research published in the journal. To help with this goal we have a checklist of factors that can help you to review the paper. We understand that there are certain cases where some checklist items may be impossible or inappropriate, but where reviewers request a checklist item and authors do not comply or provide what we consider a reasonable excuse, this may be taken into account in the final editorial decision.

We believe that the points regarding dataset and model descriptions should be fulfilled by all papers using ML.,T the points relating to reproducibility are strong suggestions meaning that we believe that they should be followed, unless there are valid reasons for not doing so (e.g. sensitive data). Much of this checklist has been adapted from 

* [Best practices in machine learning for chemistry](https://static-content.springer.com/esm/art%3A10.1038%2Fs41557-021-00716-z/MediaObjects/41557_2021_716_MOESM1_ESM.pdf)
* [The machine learning reproducibility checklist](https://www.cs.mcgill.ca/~jpineau/ReproducibilityChecklist.pdf)
* [The REFORMS checklist](https://reforms.cs.princeton.edu/appendices.pdf) 

## Dataset descriptions
### Required:
* Source(s) of data, separately for the training and evaluation datasets (if applicable), along with the time when the dataset(s) are collected 
* Number of samples in the dataset
* The details of train / validation / test splits  
* An explanation of any data that were excluded, and all pre-processing steps
* An evaluation of the amount of removed source data is reported
* Instances of combining data from multiple sources clearly identified, and potential issues mitigated
* Methods for representing data as features or descriptors clearly articulated, ideally with software implementations
##Model descriptions
### Required:
* Detailed descriptions of all models trained, including:
	* All features used in the model (including any feature selection)
	* Types of models implemented (e.g., Random Forests, Neural Networks)
	* Loss function used 
* Justification for the choice of model types implemented
* For the model(s) reported in the paper, specify details about the hyperparameter tuning:
	* Method to select the best hyper-parameter configuration
	* Specification of all hyper-parameters used to generate results reported in the paper
* Justification that any model comparisons are against appropriate baselines.
* Discussion of any possible paths for data leakage and possible impact on assessment (e.g., hyperparameter optimization using whole database before train/test split). 
## Reproducibility and Usability
### Strongly suggest:
* Open dataset used for training and evaluating the model along with link or DOI to uniquely identify the dataset (such as FigShare, Zenodo etc.)
* Open code used to train and evaluate the model and produce the results reported in the paper along with link or DOI/hash-id to uniquely identify the version of the code used
* Where relevant benchmarks and benchmarking frameworks are available, a report of the performance of the model on the benchmark data (such as JARVIS-Leaderboard, MatBench, OpenCatalyst).
* Description of the computing infrastructure used
	* Hardware infrastructure: CPU, GPU, RAM, disk space etc.
	* Operating system
	* Software environment: Programming language and version, documentation of all packages used along with versions and dependencies (e.g., through a requirements.txt/environment.yaml/nix/docker file)
	* An estimate of the time taken to generate the results
* Saved experimental data traces for automated experiments, e.g. sequence of data files and model states with the absolute or relative timestamps
* Artifacts (e.g. predicted properties, generated structures etc) produced by the model and used as results in the manuscript made available
* Any provided data should be in a recognised and usable format
* Discussion of model domain of applicability, if practical

### Nice to have:
* A cloud-based implementation of the code (e.g. JARVIS-Leaderboard, Colab, Huggingface, Garden, etc)
* As much uncertainty quantification of the model as practical

