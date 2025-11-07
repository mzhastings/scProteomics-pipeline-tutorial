MetaMorpheus Setup

## Installation
- Download [MetaMorpheus](https://github.com/smith-chem-wisc/MetaMorpheus?tab=readme-ov-file)

## Running MetaMorpheus
- Input: `.raw` spectra files, `.fasta` protein database
- Output: `AllPeptides.psmtsv`, `AllProteinGroups.psmtsv`, `AllPSMs.psmtsv`

## Walkthrough:
Databases: Drag and drop `.fasta` database and `+ADD DEFAULT CONTAMINANTS`
![Database](../assets/images/MM_Database.png)

Spectra: Drag and drop `.raw` spectra files
![Spectra](../assets/images/MM_Spectra.png)

Tasks: 
![Tasks](../assets/images/MM_Tasks.png)
- Task 1 `+ADD CALIBRATION` default
- Task 2 `+AVERAGE SPECTRA` default
- Task 3 `+ADD PTM DISCOVERY` with defaults and selection of Trypsin Digested modifications
    ![GPTMD](../assets/images/MM_GPTMD.png)
- Task 4 `+ADD SEARCH` with no quantification (quantification performed separately in FlashLFQ)
    ![Search](../assets/images/MM_Search.png)

Run: `RUN METAMORPHEUS` change output folder if desired
![Run](../assets/images/MM_Run.png)

Next up: [Quant with FlashLFQ + PIP-ECHO](./flashlfq_pipecho.md)