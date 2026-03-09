This repository for data used in the paper "Linguistic Repetition & Entropy: Observations on the Progression of Task-based Conversation", by Anaïs Claire Murat & Carl Vogel -- Trinity College Dublin.

Currently, the paper is under review at: Frontiers Journal, Research Topic ["Beyond Sequence Analysis: Integrating Quantitative Methods into Conversation Analysis"](https://www.frontiersin.org/research-topics/70123/beyond-sequence-analysis-integrating-quantitative-methods-into-conversation-analysis).

The data reuses the "transaction" and "move" annotations of the HCRC Map Task Corpus, that belongs to the University of Edinburgh and is documented and available on their website [https://groups.inf.ed.ac.uk/maptask/#nxt].

The data available here is a processed subset of the corpus, and takes the shape of a csv file named HCRC_ConversationProgression_MurataVogel.csv .

It includes 26743 rows, where each row is a turn of the HCRC dataset, and 16 columns:


- ConvID: the ID of the conversation
- ConvIndex: chronologically indexes the turn in the conversation
- turn: the content of the turn.
- DA: the dialogue act (or "move") for the given turn
- BIGDA: supra-categories of dialogue acts, as justified in the paper.
- {X, OC, CC}_{self, other}_jaccard_index: considering _all (X)_ tokens, or only _Open-class (OC)_ or _Closed-Class (CC)_ tokens, the amount of _self_ or _other_ repetitions calculated after a jaccard-index-like computation.
- entropy_speaker: shows the entropy calculation over the speaker dictionary only.
- entropy_conv: show the entropy calculation over the conversation dictionary.
- entropy_ratio: corresponds to the ratio entropy_speaker/entropy_conv.
- entropy_context: corresponds to the category of entropy dictated by the entropy ratio.
- repetition_binary: indicates the presence or absence (0) of every type of repetition. Useful for category-testing like chi-square tests.

Note: as explained in the paper, entropy is calculated over tokens that have been uttered from the start of the conversation to the present turn (included). In summary, it estimates the distribution of tokens over a bag that includes all the tokens uttered by the current speaker (_entropy_speaker_) or all the participants (_entropy_conv_).





