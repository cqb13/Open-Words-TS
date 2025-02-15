# Open Words

# **IMPORANT**

This project will no longer be maintained. A continutation of this project in rust can be found [here](https://github.com/cqb13/vocab-vault).

-----------------

Open Words TS is a port of [Open Words](https://github.com/ArchimedesDigital/open_words) Python code to Typescript for future maintenance and improvement.
Open Words is a port Of William Whitaker's original ada code to python.

Find the original Whitaker's Words written in Ada at https://github.com/dsanson/Words, thoughtfully documented and maintained by [dsanson](https://github.com/dsanson).  More information about William Whitaker and the Words program is available there.  


## Usage

Use the `Parser` class as follows:

### first value:
    String to search

### second value:
    lte: Latin to English
    etl: English to Latin

### third value:
    format answer

```
import { Parser } from './src/parser';

const parser = new Parser();

let output: any = parser.parseLine("Sunt geminae Somni portae", "lte", true);
let jsonOutput = JSON.stringify(output, null, 2);

console.log(jsonOutput);
```

````
>>>> [{'defs': [{'orth': ['sunt'], 'senses': ['to be, exist', 'also used to form verb perfect passive tenses with NOM PERF PPL'], 'infls': [{'form': {'form': 'PRES ACTIVE IND 3 P'}, 'ending': '', 'pos': 'verb'}]}], 'word': 'sunt'}, {'defs': [{'orth': ['gemin', 'gemin'], 'senses': ['twins (pl.)'], 'infls': [{'form': {'number': 'plural', 'declension': 'nominative', 'gender': 'neuter'}, 'ending': 'a', 'pos': 'noun'}, {'form': {'number': 'plural', 'declension': 'vocative', 'gender': 'neuter'}, 'ending': 'a', 'pos': 'noun'}, {'form': {'number': 'plural', 'declension': 'accusative', 'gender': 'neuter'}, 'ending': 'a', 'pos': 'noun'}, {'form': {'voice': 'active', 'person': 2, 'tense': 'present', 'mood': 'imperative', 'number': 'singular'}, 'ending': 'a', 'pos': 'verb'}]}], 'word': 'geminae'}, {'defs': [{'orth': ['somnius', 'somni'], 'senses': ['dream, vision', 'fantasy, day-dream'], 'infls': [{'form': {'number': 'singular', 'declension': 'nominative', 'gender': ''}, 'ending': '', 'pos': 'noun'}, {'form': {'number': 'singular', 'declension': 'vocative', 'gender': ''}, 'ending': '', 'pos': 'noun'}, {'form': {'number': 'singular', 'declension': 'genitive', 'gender': ''}, 'ending': '', 'pos': 'noun'}, {'form': {'number': 'singular', 'declension': 'vocative', 'gender': 'masculine'}, 'ending': '', 'pos': 'noun'}, {'form': {'number': 'singular', 'declension': 'genitive', 'gender': 'masculine'}, 'ending': '', 'pos': 'noun'}]}, {'orth': ['somnos', 'somni'], 'senses': ['sleep'], 'infls': [{'form': {'number': 'singular', 'declension': 'genitive', 'gender': ''}, 'ending': 'i', 'pos': 'noun'}, {'form': {'number': 'singular', 'declension': 'locative', 'gender': ''}, 'ending': 'i', 'pos': 'noun'}, {'form': {'number': 'plural', 'declension': 'nominative', 'gender': 'C'}, 'ending': 'i', 'pos': 'noun'}, {'form': {'number': 'plural', 'declension': 'vocative', 'gender': 'C'}, 'ending': 'i', 'pos': 'noun'}, {'form': {'number': 'singular', 'declension': 'genitive', 'gender': 'neuter'}, 'ending': 'i', 'pos': 'noun'}, {'form': {'number': 'singular', 'declension': 'genitive', 'gender': 'masculine'}, 'ending': 'i', 'pos': 'noun'}, {'form': {'number': 'singular', 'declension': 'genitive', 'gender': 'C'}, 'ending': 'i', 'pos': 'noun'}]}], 'word': 'somni'}, {'defs': [{'orth': ['porta', 'portae'], 'senses': ['gate, entrance', 'city gates', 'door', 'avenue', 'goal (soccer)'], 'infls': [{'form': {'number': 'singular', 'declension': 'genitive', 'gender': 'C'}, 'ending': 'ae', 'pos': 'noun'}, {'form': {'number': 'singular', 'declension': 'locative', 'gender': 'C'}, 'ending': 'ae', 'pos': 'noun'}, {'form': {'number': 'singular', 'declension': 'dative', 'gender': 'C'}, 'ending': 'ae', 'pos': 'noun'}, {'form': {'number': 'plural', 'declension': 'nominative', 'gender': 'C'}, 'ending': 'ae', 'pos': 'noun'}, {'form': {'number': 'plural', 'declension': 'vocative', 'gender': 'C'}, 'ending': 'ae', 'pos': 'noun'}]}], 'word': 'portae'}]

````


## Developing

Nomenclature and organization for the project follows the original architecture from Whitaker. Please reference issues on this repository for current development goals.


## Morphological information

For more information related to the morphological data contained in the files in the repository, please reference the original code of Whitaker's Words and the manner in which Whitaker used to build the significant `.LAT` and `.GEN` files mentioned in the README here: https://github.com/dsanson/Words
