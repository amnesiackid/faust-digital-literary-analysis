# Faust digital literary analysis

This is a collabrated student project for Text Technology.

This project explores structural encoding, transformation, and interactive visualization of literary drama using XML technologies. 

The analyzed text are retrieved from [Textgrid Repository](https://textgridrep.org/).

## Installation

Make sure you have Anaconda or Miniconda installed.
If not, download from: https://docs.conda.io/en/latest/miniconda.html

Clone the repository:
```bash
git clone https://github.com/amnesiackid/faust-digital-literary-analysis.git
cd faust-digital-literary-analysis
```
create a new Conda environment with:

```bash
conda env create -f environment.yml
```
This will install all required packages and dependencies with the correct versions.

Once the installation is complete, activate the environment:
```bash
conda activate faust-tei
```

## Usage

You can use data_prep.ipynb to extract desired data, such as rhyme parts, word frequency, line counts, etc.

Once desired data are extracted, as shown in sample file book1_scene_stats.json, you can use [MongoDB](https://www.mongodb.com/)
 database to visualize extracted data.
## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.
