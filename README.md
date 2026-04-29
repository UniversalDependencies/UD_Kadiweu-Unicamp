# Summary

UD_Kadiweu-UNICAMP is a treebank for [Kadiwéu](https://glottolog.org/resource/languoid/id/kadi1248) (ISO-639: `kbc`), an endangered Indigenous language of Brazil. It consists of isolated sentences produced by native speakers.


# Introduction

Kadiwéu is a polysynthetic language spoken by a few hundred people in the state of Mato Grosso do Sul, Brazil. It is the only representative of the Waikurúan linguistic family in Brazil. This family includes four languages spoken in Argentina: Toba, Pilagá, Mocoví, and Abipón.

UD_Kadiweu-UNICAMP is the first treebank for a Waikurúan language in the UD collection, contributing to the documentation and computational modeling of an under-resourced language family. It is an ongoing project, currently consisting of isolated sentences produced by native speakers, most of which are translations of Portuguese sentences. Future versions will also include narratives and other genres.

# Data source

UD_Kadiweu-UNICAMP draws on *Corpus Kadiwéu – gramática pedagógica*, one of the constituency treebanks for Kadiwéu (ISO-639: `kbc`) on the Tycho Brahe Platform. In future releases, it will incorporate texts from *Corpus Kadiwéu*, the other Kadiwéu constituency treebank on this platform. These corpora, currently under development, are annotated according to an extension of the Penn Treebank scheme. They are part of the research project *Digitally annotated corpora of Brazilian Indigenous languages with automatic translation* ([DACILAT](https://bv.fapesp.br/57063)), funded by the São Paulo Research Foundation (FAPESP) under grant No. 22/09158-5. 

The first corpus consists of elicited sentences produced by native speakers of Kadiwéu. Most of these sentences are translations of Portuguese sentences from the dataset of Alencar (2021). Additional sentences include translations of ad hoc Portuguese prompts and examples constructed by native speakers to illustrate specific aspects of the language. This material will serve as the basis for the development of a computational and a pedagogical grammar of the language. 

The second corpus comprises myths orally narrated by native speakers and transcribed using a standardized orthography by a member of the DACILAT project, a PhD student in linguistics at UNICAMP and a native speaker of Kadiwéu. 
 
## Annotation

A small set of sentences was first annotated manually to guide the development of an automatic converter in Python. In successive iterations, this tool was applied to generate draft CoNLL-U annotations for new sentences, using information from previously revised UD sentences and from the JSON dump of the constituency treebank on the Tycho Brahe Platform.

The output was subsequently refined through validation with the UD validator and manual correction of the detected issues. These corrections, together with insights from the linguistic literature on Kadiwéu, were used to improve the converter in further iterations.

All sentences were then carefully revised and checked against the original JSON data and the linguistic literature on Kadiwéu.

## Tools

For the development of UD_Kadiweu-UNICAMP, a series of Python scripts have been implemented. These scripts perform, among others, the following tasks:

- Inspecting the JSON dump of a constituency treebank from the Tycho Brahe Platform and converting it into a more human-friendly TXT format.

- Detecting inconsistencies in the original treebank annotation.

- Exploring the Kadiwéu JSON lexicon of the Tycho Brahe Platform.

- Creating draft CoNLL-U files from JSON dumps of constituency treebanks from the Tycho Brahe Platform.

- Comparing the baseline output of the converter with an improved version and with the manually revised UD treebank.

The development of these tools, as well as of UD_Kadiweu-UNICAMP, is being carried out in a separate repository:

https://github.com/leoalenc/kadiweu

# Acknowledgments

The construction of this treebank has been funded by the São Paulo Research Foundation (FAPESP), through the [DACILAT](https://bv.fapesp.br/57063) project under grant No. 22/09158-5. It is part of the post-doctoral research of Leonel Figueiredo de Alencar at the Department of Linguistics of the State University of Campinas (UNICAMP), under the supervision of Filomena Spatti Sandalo and in collaboration with Charlotte Chambelland Galves. 

We are much indebted to the speakers of Kadiwéu for sharing their knowledge of their language and for providing translations and acceptability judgements on constructed sentences. 


## References

- Sandalo, F., Pires, V., Galves, C., Silva, H., Francisco, O., & Silva, S. (2024). *Corpus Kadiwéu*. In L. Veronesi & C. Galves (Eds.), *The Tycho Brahe Platform*. Retrieved from https://www.tycho.iel.unicamp.br/

- Sandalo, F., Pires, V., Galves, C., Silva, H., Francisco, O., & Silva, S. (2024). *Corpus Kadiwéu – gramática pedagógica*. In L. Veronesi & C. Galves (Eds.), *The Tycho Brahe Platform*. Retrieved from https://www.tycho.iel.unicamp.br/

- Alencar, L. F. de. (2021). Uma gramática computacional de um fragmento do nheengatu / A computational grammar for a fragment of Nheengatu. *Revista de Estudos da Linguagem, 29*(3), 1717–1777. https://doi.org/10.17851/2237-2083.29.3.1717-1777


# Changelog

* 2026-05-15 v2.18
  * Initial release in Universal Dependencies.


<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.18
License: CC BY-NC-SA 4.0
Includes text: yes
Parallel: no
Genre: grammar-examples
Lemmas: manual native
UPOS: manual native
XPOS: manual native
Features: manual native
Relations: manual native
Contributors: Sandalo, Filomena Spatti; de Alencar, Leonel Figueiredo; Galves, Charlotte Chambelland; Veronesi, Luiz; Zeman, Daniel
Contributing: elsewhere
Contact: sandalo@unicamp.br, leonel.de.alencar@ufc.br
===============================================================================
</pre>
