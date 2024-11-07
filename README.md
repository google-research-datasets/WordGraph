# WordGraph


The WordGraph dataset contains multilingual lexicon entries linked to wikipedia entities, focusing on human-denoting names and demonym adjectives.
Each lexicon entries contain inflected word-form and morphological information all locales.


Each file contains data for one language. File name format is XX_wikidata‧tsv where XX is the two letter code for the language.


Files are tsv file with the following field:


- **topic**: the wikidata sense entry (represented by its Q id), for example: Q1410 for Gibraltar
- **relation**: the lexico-semantic relation between the topic and the entry. It can be:
    - *Demonym noun*: the noun referring to the inhabitants of a location or the member of an ethnic group (e‧g. "Gibraltarian" for "Gibraltar")
    - *Demonym adjective*: the adjective describing a relation with a location or an ethnic group
    - *Human denoting sense*: the noun referring to a topic that describes a human activity or a role (like "hairdresser", "king", "friend"). These entries are particularly useful to provide male/female forms for these roles/professions. 
- **language**: the Q id for the language
- **pos**: the Part-of-Speech. In these resources, only "Nominal" or "Adjectival" are available
- **lemma**: the lemma of the entry.
- **orthography**: one of the form of the entry.
- **features**: the Q id of the morphosyntactic structures describing the orthography

Each entry can be reconstructed by grouping all the lines that contain the same lemma and the same POS:

> Topic: Q187985               # Tibet
> 
> Relation:  Demonym noun
>
> Language: Q150         #French
>
> POS: nominal
>
> Lemma: tibétain
>
> Forms:
> - tibétain	Q110786,Q499327 #singural, #masculine
> - tibétaine	Q110786,Q1775415 #singural, #feminine
> - tibétains	Q146786,Q499327 #plural, #masculine
> - tibétaines	Q146786,Q1775415 #plural, #feminine
>



