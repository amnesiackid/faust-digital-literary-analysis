# Faust digital literary analysis

This is a collabrated student project for Text Technology.

This project explores structural encoding, transformation, character network analysis and interactive visualization of literary drama using XML technologies and Python-based tools. 

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

The database schemata of the resulting database is:
```jsonc
{
  "scene_num": "Int",          // Scene number
  "scene_title": "Str",         // Scene title, eg. "Nacht."
  "speakers": {                  // Speakers in the scene
    "SPEAKER_NAME": {           // Speaker name
      "lines": "Int",          // Line counts of the speaker
      "word_freq": {             
        "word": "Int",         // Word frequency of non stop words
        "..."
      }
    },
    "..."
  }
}
```

A presentation of the textual data is shown in faust_web.html

Once desired data are extracted, as shown in sample file book1_scene_stats.json, you can use [MongoDB](https://www.mongodb.com/)
 database to visualize extracted data.


You can also run `Faust_TEI_Full_Processing.ipynb` to extract scenes, speakers, and poetic lines from the TEI XML. This notebook enhances each scene by adding attributes such as `rhyme_ends` (the final words in poetic lines), `speakers_unique` (a list of unique characters), and `speaker_freq` (character frequency per scene).

The script also generates word frequency data and calculates speaker co-occurrence across scenes. Output files include `faust_characters_nodes.csv`, `faust_character_cooccurrence.csv`, `faust_scene_character.csv`, and `faust_total_wordfreq.csv`. These can be visualized using `networkx` or imported into Neo4j for further network analysis.

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.
