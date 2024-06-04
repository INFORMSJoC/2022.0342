[![INFORMS Journal on Computing Logo](https://INFORMSJoC.github.io/logos/INFORMS_Journal_on_Computing_Header.jpg)](https://pubsonline.informs.org/journal/ijoc)

# Learning Hidden Markov Models with Structured Transition Dynamics

This archive is distributed in association with the [INFORMS Journal on
Computing](https://pubsonline.informs.org/journal/ijoc) under the [MIT License](LICENSE).

The software and data in this repository are a snapshot of the software and data
that were used in the research reported on in the paper 
[Learning Hidden Markov Models with Structured Transition Dynamics](https://doi.org/10.1287/ijoc.2022.0342) by S. Ma, A. Dehganian, G.-G. P. Garcia, and N. Serban. 


## Cite

To cite the contents of this repository, please cite both the paper and this repo, using their respective DOIs.

https://doi.org/10.1287/ijoc.2022.0342

https://doi.org/10.1287/ijoc.2022.0342.cd

Below is the BibTex for citing this snapshot of the respoitory.

```
@misc{LearningHMMs_repo,
  author =        {Ma, Simian and Dehganian, Amin and Garcia, Gian-Gabriel P, and Serban, Nicoleta},
  publisher =     {INFORMS Journal on Computing},
  title =         {{Learning Hidden Markov Models with Structured Transition Dynamics}},
  year =          {2024},
  doi =           {10.1287/ijoc.2022.0342},
  url =           {https://github.com/INFORMSJoC/2022.0342},
  note =          {Available for download at https://github.com/INFORMSJoC/2022.0342},
}  
```

## Description

The goal of this code is to fit a Hidden Markov Model (HMM) to data with multiple linear constraints imposed on the HMM's transition and emission probability matrices via the LDKB-FISTA algorithm. Alongside our LDKB-FISTA, we have also uploaded the scripts for running Matlab-Fimincon method, as well as the traditional Baum Welch method.
The code are written in Matlab.

### How to use it
**Data Description**

The data folder contains simulated data related to sports-related concussions. The CSV files are named according to the following convention: gender (male/female), concussion history (0-2 concussions or 3+ concussions), and the type of score (SCATSEV or SAC). For example, a file named SAC_category_F_Hx02.csv contains SAC scores for females with 0-2 concussions. For more detailed information about the sports-related concussion data, please refer to the accompanying manuscript.

**Running the LDKB-FISTA Algorithm**

Our implementation of the LDKB-FISTA algorithm is provided in the Matlab script LDKBFISTA.m. To use the script, follow these steps:

**Open the Script** 

Open the LDKBFISTA.m file in Matlab.
Specify the Input Files: Modify the script to specify the input files you wish to analyze. For example, to estimate the transition and emission probability matrices for females with 0-2 concussion history, set the input files to SAC_category_F_Hx02.csv and SCATSEV_category_F_Hx02.csv.

**Run the Script**

Execute the script in Matlab. The output transition and emission probability matrices will be saved as two separate CSV files in the same directory.

Running the Comparing Methods
The methods for comparison, Fmincon and Baum Welch, can be executed in a similar manner. Open the respective Matlab scripts, specify the input files, and run the scripts.

## Replicating the Experiments

To replicate the experiments presented in our manuscript, follow these steps:

**Run LDKBFISTA.m**

Execute the LDKBFISTA.m script for each of the four sports-related concussion groups (male/female with 0-2/3+ concussions).

**Obtain the Estimated Matrices**

For each group, obtain the estimated transition and emission probability matrices.

**Compute Predictive Distributions**

Using the learned Hidden Markov Model (HMM) parameters, compute the predictive distributions.
For more details on the evaluation process, please refer to Appendix J of the manuscript.

**Additional Information**
For further details and comprehensive explanations, please refer to the manuscript. If you have any questions or encounter any issues, feel free to contact the authors.


### Data

Note that the data included in this repository is a synthetic version of the data used in our analysis. We provide synthetic data because the FITBIR data cannot be shared publicly. However, the NCAA-DoD CARE dataset is available in the FITBIR database (https://fitbir.nuh.gov/) following an approved data request.

