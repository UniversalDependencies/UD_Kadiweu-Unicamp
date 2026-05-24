# Summary

UD_Kadiweu-Unicamp is a treebank for [Kadiwéu](https://glottolog.org/resource/languoid/id/kadi1248) (ISO-639: `kbc`), an endangered Indigenous language of Brazil. It consists of isolated sentences produced by native speakers.


# Introduction

Kadiwéu is a polysynthetic language spoken in the state of Mato Grosso do Sul, Brazil. It is severely endangered: among approximately 1,500 Kadiwéu people, fewer than 300 speak the language, as many have shifted to Portuguese (Pires 2022). Kadiwéu is the only representative of the Waikurúan linguistic family in Brazil. This family includes four additional languages: Toba, Pilagá, and Mocoví, mostly spoken in Argentina, and Abipón, formerly spoken in Argentina but now extinct (Sandalo 1995).

UD_Kadiweu-Unicamp is the first treebank for a Waikurúan language in the UD collection, contributing to the documentation and computational modeling of a poorly documented and under-resourced language family. It is an ongoing project, currently consisting of isolated sentences produced by native speakers, most of which are translations of Portuguese sentences. Future versions will also include narratives and other genres.

# Data source

UD_Kadiweu-Unicamp draws on *Corpus Kadiwéu – gramática pedagógica* (Sandalo et al. 2024b), one of the constituency treebanks for Kadiwéu (ISO-639: `kbc`) on the Tycho Brahe Platform. In future releases, it will incorporate texts from *Corpus Kadiwéu* (Sandalo et al. 2024a), the other Kadiwéu constituency treebank on this platform. These corpora, currently under development, are annotated according to an extension of the Penn Treebank scheme (Galves et al. 2017, Sandalo & Galves 2023). They are part of the research project *Digitally annotated corpora of Brazilian Indigenous languages with automatic translations* ([DACILAT](https://bv.fapesp.br/57063)), funded by the São Paulo Research Foundation (FAPESP) under grant No. 22/09158-5. 

The first corpus consists of elicited sentences produced by native speakers of Kadiwéu. Most of these sentences are translations of Portuguese sentences from the dataset of Alencar (2021). Additional sentences include translations of ad hoc Portuguese prompts and examples constructed by native speakers to illustrate specific aspects of the language. This material will serve as the basis for the development of a computational and a pedagogical grammar of the language. 

The second corpus comprises myths orally narrated by native speakers and transcribed using a standardized orthography by a member of the DACILAT project, a PhD student in linguistics at UNICAMP and a native speaker of Kadiwéu. 
 
## Annotation

A small set of sentences was first annotated manually to guide the development of an automatic converter in Python. An initial version of this tool was applied to generate draft CoNLL-U annotations for new sentences, using information from the JSON dump of the constituency treebank on the Tycho Brahe Platform.

In successive iterations, the converter was improved through validation of its output with the UD validator and manual correction of the detected issues. Fully validated sentences were periodically selected from the draft CoNLL-U, manually revised, and added to the gold treebank, taking into account the original JSON data and the linguistic literature on Kadiwéu. Information about lemmatization and features from these gold sentences was fed back into the converter.

In some cases, the application of the converter or the revision of its output revealed incorrect or incomplete annotation in the source data. These cases were corrected in the Tycho Brahe Platform, and revised JSON dumps were generated.

This inaugural release of UD_Kadiweu-Unicamp includes 71 sentences out of a total of 203 from *Corpus Kadiwéu – gramática pedagógica* (Sandalo et al. 2024b). Fully revised sentences will be continually added to the development version of the treebank in the coming months.

## Tools

For the development of UD_Kadiweu-Unicamp, a series of Python scripts have been implemented. These scripts perform, among others, the following tasks:

- Inspecting the JSON dump of a constituency treebank from the Tycho Brahe Platform and converting it into a more human-friendly TXT format.

- Detecting inconsistencies in the original treebank annotation.

- Exploring the Kadiwéu JSON lexicon of the Tycho Brahe Platform.

- Creating draft CoNLL-U files from JSON dumps of constituency treebanks from the Tycho Brahe Platform.

- Comparing the baseline output of the converter with an improved version and with the manually revised UD treebank.

The development of these tools, as well as of UD_Kadiweu-Unicamp, is being carried out in a separate repository:

https://github.com/leoalenc/kadiweu

# Acknowledgments

The construction of this treebank has been funded by the São Paulo Research Foundation (FAPESP) through the [DACILAT](https://bv.fapesp.br/57063) project (grant No. 22/09158-5). It is part of the postdoctoral research of Leonel Figueiredo de Alencar at the Department of Linguistics of the State University of Campinas (UNICAMP), under the supervision of Filomena Spatti Sandalo, coordinator of the DACILAT project, and in collaboration with Charlotte Chambelland Galves. 

We are much indebted to the speakers of Kadiwéu for sharing their knowledge of their language and for providing translations and acceptability judgements on constructed sentences. 


## References

- Alencar, L. F. de. (2021). Uma gramática computacional de um fragmento do nheengatu / A computational grammar for a fragment of Nheengatu. *Revista de Estudos da Linguagem, 29*(3), 1717–1777. https://doi.org/10.17851/2237-2083.29.3.1717-1777

- Galves, C., Sandalo, F., Sena, T. A. de, & Veronesi, L. (2017). Annotating a polysynthetic language: From Portuguese to Kadiwéu. *Cadernos de Estudos Linguísticos, 59*(3), 631–648. https://doi.org/10.20396/cel.v59i3.8651003

- Pires, V. (2022). *Palavras kadiwéu do mundo ancestral e do mundo novo: palavras novas, palavras antigas, palavras humildes e palavras honorificadas* (Master’s thesis). Universidade Estadual de Campinas. https://hdl.handle.net/20.500.12733/4592

- Sandalo, F. (1995). *A grammar of Kadiwéu* (PhD dissertation). University of Pittsburgh.

- Sandalo, F., & Galves, C. (2023). Anotando sintaticamente uma língua originária do Brasil: O problema de Anchieta. *Cadernos de Estudos Linguísticos, 65*, e023007. https://doi.org/10.20396/cel.v65i00.8673592

- Sandalo, F., Pires, V., Galves, C., Silva, H., Francisco, O., & Silva, S. (2024a). *Corpus Kadiwéu*. In L. Veronesi & C. Galves (Eds.), *The Tycho Brahe Platform*. https://www.tycho.iel.unicamp.br/

- Sandalo, F., Pires, V., Galves, C., Silva, H., Francisco, O., & Silva, S. (2024b). *Corpus Kadiwéu – gramática pedagógica*. In L. Veronesi & C. Galves (Eds.), *The Tycho Brahe Platform*. https://www.tycho.iel.unicamp.br/


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
