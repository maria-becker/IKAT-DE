Enriching Argumentative Texts with Implicit Knowledge

Maria Becker, Michael Staniek, Vivi Nastase, and Anette Frank
contact: mbecker@cl.uni-heidelberg.de

Short project description/Abstract. Retrieving information that is implicit in a text is difficult. For argument analysis, revealing implied knowledge could be useful to judge how solid an argument is and to construct concise arguments. We design a process for obtaining high-quality implied knowledge annotations for German argumentative microtexts, in the form of simple natural language statements. This process involves several steps to promote agreement and monitors its evolution using textual similarity computation. To further characterize the implied knowledge, we annotate the added sentences with semantic clause types and common sense knowledge relations. To test whether the knowledge could be retrieved automatically, we compare the inserted sentences to Wikipedia articles on similar topics. Analysis of the added knowledge shows that (i) it is characterized by a high proportion of generic sentences, (ii) a majority of it can be mapped to common sense knowledge relations, and (iii) it is similar to sentences found in Wikipedia.

For details or questions, please read our paper (Becker et al. 2017) or contact me by mail (mbecker@cl.uni-heidelberg.de).


ANNOTATION OF IMPLICIT KNOWLEDGE. The annotations are performed on sentence pairs from the Microtext corpus (the original German version, Peldszus/Stede 2015), that stand in an argumentative relation according to the argumentation graph. There are 464 such sentence pairs in the 112 texts in the corpus, i.e., approx. 4 pairs per microtext. All annotations of described below are stored in the folder „Annotations_Implicit_Knowledge“.

Step 1: H1 and H2 produce initial annotations A1 and A2. The annotators are asked to add the minimal amount of information that makes the connection between the two sentences explicit by: (1) adding as few sentences as possible and (2) making the inserted sentences as simple as possible so that they ideally only contain one fact per sentence. Through these instructions we intend to avoid long and too detailed explanations, and in consequence, to support better agreement between the judges. If the annotators think that no information is missing (i.e., the connection between sentences is explicit), this is labeled correspondingly.

Step 2: H1 and H2 review each other’s annotations, producing corrected versions: H1(A2)=A2_c, H2(A1)=A1_c.

Step 3: To avoid biases arising from the correction phase, two different judges H3 and H4 independently perform merges of A1_c and A2_c, producing annotations A3 and A4, respectively. They are allowed to select one annotation, combine them into a novel statement, or to produce a new annotation. 

Step 4: A final annotator H5 produces the gold standard based on A3 and A4 following the merge process described above, with the difference that for this final step we allow two versions of the inserted information if both of them fill the gap. 

The annotation process is described in more detail in Becker et al. 2017.

ANNOTATION OF SITUATION ENTITY TYPES. We asked the annotators to characterize the inserted sentences by labeling them with situation entity types (Smith 2003, Friedrich et al. 2016):

- states describe specific properties of individuals
- events are things that happen or have happened
- generic sentences are predicates over classes or kinds
- generalizing sentences describe regularly occurring events or habits

The annotations are performed independently by two trained annotators and a third expert annotator who assigned the GOLD label. They assign SE type labels at the clause level.

The data annotated with SE types is stored in the folder „Annotations_Situation_Entities“.

ANNOTATION OF CONCEPTNET RELATIONS. To gain further insight into the type of knowledge covered by the provided sentences, we annotate them with ConceptNet relation types such as PartOf, Causes or IsA. 
The annotation was performed by two annotators in parallel  and a third expert annotator who assigned the GOLD label. They were asked to label each inserted sentence, if applicable.

The data annotated with ConceptNet relations is stored in the folder „Annotations_Situation_Entities“.

RETRIEVING SIMILAR SENTENCES FROM WIKIPEDIA. The annotations of implied knowledge represent a gold standard that should be obtainable automatically, whether in their exact form or as approximations. We test whether the implied knowledge that the annotators made explicit through the provided sentences can be found in a textual corpus.
We collect a corpus of Wikipedia sentences from articles that match the topics of the microtexts in the Microtext corpus. Each microtext was elicited with a query, e.g. Should Germany introduce the death penalty?. We match this query to German Wikipedia article titles and extract the introduction section of the article, if it exists, or the first 10 sentences. From all 18 queries used in to produce the corpus, we find matches for 50 related topics such as tuition fees or waste separation, resulting in a corpus of 874 sentences.
To test whether we can find sentences in Wikipedia that match sentences in the inserted information set, we use the distance formula WMD′ (Becker et al. 2017, equation 2).

The sentences retrieved from Wikipedia together with their distance scores are stored in the folder „Wikipedia_Most_Similar_Sentences“.

In the file "IKAT_all_annotations_in_one_file.txt" all annotations are merged and linked to the argumentative microtexts.

References:

Becker, M., Staniek, M., Nastase, V., Frank, A. (2017): Enriching Argumentative Texts with Implicit Knowledge. International Conference on Natural Language & Information Systems (NLDB).

Annemarie Friedrich, Alexis Palmer, and Manfred Pinkal. 2016. Situation entity types: automatic classification of clause-level aspect. In Proceedings of ACL 2016.

Andreas Peldszus and Manfred Stede. 2015. An an- notated corpus of argumentative microtexts. In Proceedings of the First European Conference on Argumentation: Argumentation and Reasoned Action.

Carlota S Smith. 2003. Modes of discourse: The local structure of texts, volume 103. Cambridge University Press.
