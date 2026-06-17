# Extractive Text Summarization with BERT Extractive Summarizer

- **Source URL:** https://www.holisticseo.digital/python-seo/summarize/
- **Domain:** www.holisticseo.digital

--- 

Extractive Text Summarization with BERT Extractive Summarizer involves summarizing an article with the extracted key information via BERT natural language model. Extractive summarization is to provide decreased memory usage while protecting the content’s value. Information about the content is protected via extractive summarizers. BERT is used to understand human languages via RNN, Attention mechanisms, and Transformers. BERT extractive summarization provides control over the summarization’s sentence count and character count. Extractive summarization chooses the most prominent sentences, and meaningful entities to describe the overall meaning of a document.



BERT Sentence embeddings provide building an extractive summarize method via the TextRank model and Lead3. BERT is used for understanding an article’s internal structure. The unsupervised TextRank Model is used to select sentences based on the corpus’ inferior nature. Lead3 is used by many other content publishers as a method for summarizing articles. Lead3 means using the first 3 sentences to summarize the entire document. Thus, the title of the document and the last heading, and sentence pairs of the document stay in harmony. Lead3 approach takes the sequential information from the article to create an extractive summary of the text.

**Contents of the Article** [show](#)

- [1. What is Extractive Summarization?](#What-is-Extractive-Summarization)

- [1.1. What are the Obstacles to Extractive Summarization?](#What-are-the-Obstacles-to-Extractive-Summarization)
- [1.2. What are the helpful methods for Extractive Summarization Scoring?](#What-are-the-helpful-methods-for-Extractive-Summarization-Scoring)
- [2. How to Summarize Articles with BERT Extractive Summarizer?](#How-to-Summarize-Articles-with-BERT-Extractive-Summarizer)
- [3. What are the Configuration Parameters for BERT Extractive Text Summarizer?](#What-are-the-Configuration-Parameters-for-BERT-Extractive-Text-Summarizer)
- [4. What are the uses of the BERT Extractive Text Summarizer?](#What-are-the-uses-of-the-BERT-Extractive-Text-Summarizer)
- [5. What are the Other Relevant Articles for BERT Extractive Text Summarizer?](#What-are-the-Other-Relevant-Articles-for-BERT-Extractive-Text-Summarizer)
- [6. Last Thoughts on BERT Extractive Text Summarizer and Holistic SEO](#Last-Thoughts-on-BERT-Extractive-Text-Summarizer-and-Holistic-SEO)


## What is Extractive Summarization?



Extractive summarization is a method to extract the key sentences from an article to summarize the meaning of the text. Extractive summarization is the alternative to abstraction summarization. Extractive and abstractive summarization the main difference is that extractive summarization uses the sentences from the existing text, while abstractive summarization generates new sentences to summarize the article. The best text that summarizes mixes both extractive and abstractive summarization. Extractive summarization methodologies are used for binary classification problems.



### What are the Obstacles to Extractive Summarization?



The abstractive summarization main obstacle is finding enough levels of data. Most of the time, even if there is a proper extractive summarization with BERT or with another NLP Algorithm model, still measuring the efficiency of the specific extractive summarization is hard due to the data deficiency. Thus, most of the extractive summarization research use news articles, or scientific research. Because, scientific research and news articles provide a topicality, and a roundup of the article at the beginning. This gives a possibility to compare the specific article’s summary to the real summary for scoring.



### What are the helpful methods for Extractive Summarization Scoring?



To score an extractive summary sample, the methods and metrics along with the tools below are used.



- Rouge-N is the measure to calculate the overlapping N-Gram occurrences between the existing summary of the text and the extractive summary output with BERT-extractive-summarizer or other models.
- Rouge Recall is to normalize the overlapping N-Gram value count by the length of the summaries.
- Rouge Precision is to increase the precision of the specific summary by comparing its length and unnecessary and contextless word count to the specific summary.
- Rouge-l F1 is to provide a harmonic meaningful precision.
- Rouge-L is to provide a stricter quality score for the extractive summarization.
- Sentence Ranking is to rank the sentences based on their possibility to be a part of the summary.
- Confusion Matrix is to compare the consequence of the sentence ranking and the Rouge methods for the extractive text summarizer’s success.


## How to Summarize Articles with BERT Extractive Summarizer?



To summarize articles with NLP and BERT Extractive Summarizer, use the code block below.



- Download the necessary dependencies for BERT Extractive Summarizer. These are “bert-extractive-summarizer”, “spacy”, “transformers”, “neuralcoref”.


```
!pip install -q bert-extractive-summarizer
!pip install -q spacy
!pip install -q transformers
!pip install -q neuralcoref
```



If the related dependencies are not ready on your computer, use the code block below.



2. Import the “Summarizer from summarizing” and import the “pprint” for pretty-printing the summary of the text.



```
from summarizer import Summarizer
from pprint import pprint
```



Above, to perform an extractive summarization via BERT, the necessary Python modules are imported. The BERT Extractive Summarization can be used for books, articles, news stories, scientific research, product reviews, and more. In this example, we have used the “Crime and Punishment” book from Fyodor Dostoevsky to perform an extractive summarization.



```
with open("crime_and_punishment.txt", 'r', encoding="UTF-8") as file:
data = file.read().replace('\n', '')
data = data.replace("\ufeff", "")
```



3. Assign the specific novel, or the corpus content, into the specific variable for summarization.



Below, you can see the specific novel’s specific section for BERT extractive summarization.



```
data[1000:5800]

OUTPUT >>>

' work.Dostoevsky was the son of a doctor. His parents were very hard-workingand deeply religious people, but so poor that they lived with their fivechildren in only two rooms. The father and mother spent their eveningsin reading aloud to their children, generally from books of a seriouscharacter.Though always sickly and delicate Dostoevsky came out third in thefinal examination of the Petersburg school of Engineering. There he hadalready begun his first work, “Poor Folk.”This story was published by the poet Nekrassov in his review andwas received with acclamations. The shy, unknown youth found himselfinstantly something of a celebrity. A brilliant and successful careerseemed to open before him, but those hopes were soon dashed. In 1849 hewas arrested.Though neither by temperament nor conviction a revolutionist, Dostoevskywas one of a little group of young men who met together to read Fourierand Proudhon. He was accused of “taking part in conversations againstthe censorship, of reading a letter from Byelinsky to Gogol, and ofknowing of the intention to set up a printing press.” Under NicholasI. (that “stern and just man,” as Maurice Baring calls him) this wasenough, and he was condemned to death. After eight months’ imprisonmenthe was with twenty-one others taken out to the Semyonovsky Square tobe shot. Writing to his brother Mihail, Dostoevsky says: “They snappedwords over our heads, and they made us put on the white shirts worn bypersons condemned to death. Thereupon we were bound in threes to stakes,to suffer execution. Being the third in the row, I concluded I had onlya few minutes of life before me. I thought of you and your dear ones andI contrived to kiss Plestcheiev and Dourov, who were next to me, and tobid them farewell. Suddenly the troops beat a tattoo, we were unbound,brought back upon the scaffold, and informed that his Majesty had sparedus our lives.” The sentence was commuted to hard labour.One of the prisoners, Grigoryev, went mad as soon as he was untied, andnever regained his sanity.The intense suffering of this experience left a lasting stamp onDostoevsky’s mind. Though his religious temper led him in the end toaccept every suffering with resignation and to regard it as a blessingin his own case, he constantly recurs to the subject in his writings.He describes the awful agony of the condemned man and insists on thecruelty of inflicting such torture. Then followed four years of penalservitude, spent in the company of common criminals in Siberia, wherehe began the “Dead House,” and some years of service in a disciplinarybattalion.He had shown signs of some obscure nervous disease before his arrestand this now developed into violent attacks of epilepsy, from which hesuffered for the rest of his life. The fits occurred three or four timesa year and were more frequent in periods of great strain. In 1859 he wasallowed to return to Russia. He started a journal--“Vremya,” which wasforbidden by the Censorship through a misunderstanding. In 1864 he losthis first wife and his brother Mihail. He was in terrible poverty, yethe took upon himself the payment of his brother’s debts. He startedanother journal--“The Epoch,” which within a few months was alsoprohibited. He was weighed down by debt, his brother’s family wasdependent on him, he was forced to write at heart-breaking speed, and issaid never to have corrected his work. The later years of his life weremuch softened by the tenderness and devotion of his second wife.In June 1880 he made his famous speech at the unveiling of themonument to Pushkin in Moscow and he was received with extraordinarydemonstrations of love and honour.A few months later Dostoevsky died. He was followed to the grave by avast multitude of mourners, who “gave the hapless man the funeral of aking.” He is still probably the most widely read writer in Russia.In the words of a Russian critic, who seeks to explain the feelinginspired by Dostoevsky: “He was one of ourselves, a man of our blood andour bone, but one who has suffered and has seen so much more deeply thanwe have his insight impresses us as wisdom... that wisdom of the heartwhich we seek that we may learn from it how to live. All his othergifts came to him from nature, this he won for himself and through it hebecame great.”CRIME AND PUNISHMENTPART ICHAPTER IOn an exceptionally hot evening early in July a young man came out ofthe garret in which he lodged in S. Place and walked slowly, as thoughin hesitation, towards K. bridge.He had successfully avoided meeting his landlady on the staircase. Hisgarret was under the roof of a high, five-storied house and was morelike a cupboard than a room. The landlady who provided him with garret,dinners, and attendance, lived on the floor below, and every timehe went out he was obliged to'
```



4. Use the “Summarizer()” function on the “model” variable. Adjust the parameters “num_sentences” and “min_length” to determine the total summary sentence count, along with the summative sentence length.



```
model = Summarizer()
result = model(data[1000:25800], num_sentences=5, min_length=60)
full = ''.join(result)
```



5. Compare the Summarizer Output to the Normal Text



```
pprint(full)

OUTPUT >>>

('His parents were very hard-workingand deeply religious people, but so poor '
'that they lived with their fivechildren in only two rooms. He describes the '
'awful agony of the condemned man and insists on thecruelty of inflicting '
'such torture. It was a different matter when he met withacquaintances or '
'with former fellow students, whom, indeed, he dislikedmeeting at any time. '
'And yet when a drunken man who, for some unknownreason, was being taken '
'somewhere in a huge waggon dragged by a heavydray horse, suddenly shouted at '
'him as he drove past: “Hey there, Germanhatter” bawling at the top of his '
'voice and pointing at him--the youngman stopped suddenly and clutched '
'tremulously at his hat. The master of the establishment was in another room, '
'but he frequentlycame down some steps into the main room, his jaunty, tarred '
'boots withred turn-over tops coming into view each time before the rest of '
'hisperson.')
```



A second example of the BERT Extractive Summary creation is below.



Below, you can see the total text that we have summarized.



```
data[50000:52800]

OUTPUT >>>

'had, as I saw.... She saidnothing, she only looked at me without a word.... Not on earth, but upyonder... they grieve over men, they weep, but they don’t blame them,they don’t blame them! But it hurts more, it hurts more when they don’tblame! Thirty copecks yes! And maybe she needs them now, eh? What doyou think, my dear sir? For now she’s got to keep up her appearance. Itcosts money, that smartness, that special smartness, you know? Do youunderstand? And there’s pomatum, too, you see, she must have things;petticoats, starched ones, shoes, too, real jaunty ones to show off herfoot when she has to step over a puddle. Do you understand, sir, do youunderstand what all that smartness means? And here I, her own father,here I took thirty copecks of that money for a drink! And I am drinkingit! And I have already drunk it! Come, who will have pity on a man likeme, eh? Are you sorry for me, sir, or not? Tell me, sir, are you sorryor not? He-he-he!”He would have filled his glass, but there was no drink left. The pot wasempty.“What are you to be pitied for?” shouted the tavern-keeper who was againnear them.Shouts of laughter and even oaths followed. The laughter and the oathscame from those who were listening and also from those who had heardnothing but were simply looking at the figure of the dischargedgovernment clerk.“To be pitied! Why am I to be pitied?” Marmeladov suddenly declaimed,standing up with his arm outstretched, as though he had been onlywaiting for that question.“Why am I to be pitied, you say? Yes! there’s nothing to pity me for! Iought to be crucified, crucified on a cross, not pitied! Crucify me,oh judge, crucify me but pity me! And then I will go of myself to becrucified, for it’s not merry-making I seek but tears and tribulation!...Do you suppose, you that sell, that this pint of yours has beensweet to me? It was tribulation I sought at the bottom of it, tears andtribulation, and have found it, and I have tasted it; but He will pityus Who has had pity on all men, Who has understood all men and allthings, He is the One, He too is the judge. He will come in that dayand He will ask: ‘Where is the daughter who gave herself for her cross,consumptive step-mother and for the little children of another? Where isthe daughter who had pity upon the filthy drunkard, her earthly father,undismayed by his beastliness?’ And He will say, ‘Come to me! I havealready forgiven thee once.... I have forgiven thee once.... Thy sinswhich are many are forgiven thee for thou hast loved much....’ And hewill forgive my Sonia, He will forgive, I know it... I felt it in myheart when I was with her just now! And He will judge and will forgiveall, the good and the evil, the wise and the meek.... And when He hasdone with all of them, then He will summon us. ‘You too come for'
```



Another example of the BERT Extractive Text Summarization is below.



```
model = Summarizer()
result = model(data[50000:52800], num_sentences=5, min_length=60)
full = ''.join(result)
pprint(full)

OUTPUT>>>

('had, as I saw.... She saidnothing, she only looked at me without a word.... '
'Not on earth, but upyonder... they grieve over men, they weep, but they '
'don’t blame them,they don’t blame them! And here I, her own father,here I '
'took thirty copecks of that money for a drink! He-he-he!”He would have '
'filled his glass, but there was no drink left. Marmeladov suddenly '
'declaimed,standing up with his arm outstretched, as though he had been '
'onlywaiting for that question. And then I will go of myself to becrucified, '
'for it’s not merry-making I seek but tears and tribulation!...Do you '
'suppose, you that sell, that this pint of yours has beensweet to me?')
```



For the third example of the Python BERT Extractive Text Summarizer, the parameters of the “num_sentences” and the “min_length” are modified. The “number of sentences for the extractive text summarization is 10”, and the “minimum sentence length” is 120. You can check how the results change below.



```
model = Summarizer()
result = model(data[50000:52800], num_sentences=10, min_length=120)
full = ''.join(result)

OUTPUT >>>

('had, as I saw.... She saidnothing, she only looked at me without a word.... '
'Not on earth, but upyonder... they grieve over men, they weep, but they '
'don’t blame them,they don’t blame them! And there’s pomatum, too, you see, '
'she must have things;petticoats, starched ones, shoes, too, real jaunty ones '
'to show off herfoot when she has to step over a puddle. The laughter and the '
'oathscame from those who were listening and also from those who had '
'heardnothing but were simply looking at the figure of the '
'dischargedgovernment clerk. Marmeladov suddenly declaimed,standing up with '
'his arm outstretched, as though he had been onlywaiting for that question. '
'And then I will go of myself to becrucified, for it’s not merry-making I '
'seek but tears and tribulation!...Do you suppose, you that sell, that this '
'pint of yours has beensweet to me? It was tribulation I sought at the bottom '
'of it, tears andtribulation, and have found it, and I have tasted it; but He '
'will pityus Who has had pity on all men, Who has understood all men and '
'allthings, He is the One, He too is the judge. He will come in that dayand '
'He will ask: ‘Where is the daughter who gave herself for her '
'cross,consumptive step-mother and for the little children of another? I '
'havealready forgiven thee once.... I have forgiven thee once.... Thy '
'sinswhich are many are forgiven thee for thou hast loved much....’ And '
'hewill forgive my Sonia, He will forgive, I know it... I felt it in myheart '
'when I was with her just now! And He will judge and will forgiveall, the '
'good and the evil, the wise and the meek.... And when He hasdone with all of '
'them, then He will summon us. ‘')
```



Since we have performed a longer summarization, we also made the input text longer.



## What are the Configuration Parameters for BERT Extractive Text Summarizer?



The configuration parameters for BERT Extractive Text Summarizer are below.



- “num_sentences” is to provide a number of sentences for summarization.
- “min_length” is to provide the minimum length of the sentence for the summarization sentences.


The configuration parameters for the BERT NLP Extractive text summarization tools provide a better granularity and explanatory optimization for the output of the summarization.



## What are the uses of the BERT Extractive Text Summarizer?



The Extractive Text Summarizer and the BERT uses are below.



- Writing product short descriptions.
- Writing web page meta descriptions.
- Writing product reviews for the introduction of articles.
- Classification of the news articles.
- Ranking and classifying articles with lower memory usage.
- Writing unique content to help human authors.
- Decreasing the time cost of reading long articles and documents.


## What are the Other Relevant Articles for BERT Extractive Text Summarizer?



To understand BERT Extractive Text Summarizer, use the concepts and articles below.



- [Information Graph](https://www.holisticseo.digital/python-seo/information-extraction/): Entity Relation Diagram creation is beneficial for BERT Extractive Text Summarizer. Because central entities and central contexts are the key points to summarize.
- [Text Analysis](https://www.holisticseo.digital/python-seo/perform-text-analysis/): Text analysis is useful for BERT Extractive Text Summarization because it provides the heaviest terms in a text.
- [NLTK Tokenize](https://www.holisticseo.digital/python-seo/nltk/tokenization): NLTK Tokenize is helpful to understand what BERT Extractive Text Summarizer does. It provides an understanding to see how Tokenization works.
- [NLTK Lemmatize](https://www.holisticseo.digital/python-seo/nltk/lemmatize): NLTK Lemmatize is helpful to understand what BERT Extractive Text Summarizer does. It provides an understanding to see how Tokenization works.


## Last Thoughts on BERT Extractive Text Summarizer and Holistic SEO



BERT Extractive Text Summarizer is used together with PyTorch, Spacy, Neuralconf, and Transformers. BERT Extractive Text Summarizer helps Search Engine Optimization to understand how the Google search engine’s NLP Algorithms create summarization for articles. Understanding why the BERT NLP Model chooses a specific sentence, and how they rank the sentences or recognize entities, extracting the key points from a long article helps an SEO to understand the Google search engine’s possible sensitiveness and capacity to interpret a content’s quality, and prominent sections. BERT Extractive Text Summarizer is a useful technique to start learning NLP and NLP basic Python libraries such as Natural Language Tool Kit. BERT Extractive Text Summarization tools, measures, scores, and datasets are helpful for Holistic SEOs to improve their NLP Skills and Search Engine Understanding. Natural Language Processing and Extractive Summarization are part of Holistic SEO. Summarizing an article in a meta description, or hooking the reader from the beginning of an article for better UX, are connected to the NLP Extractive Text Summarization.



In this context, from content marketing to content generation or summarization, the BERT NLP Algorithms and Extractive Summarization concept and methods are helpful for Holistic SEO. The tutorial and guide for Extractive Text Summarizer will be updated in light of the new content.



- [Author](#abh_about)
- [Recent Posts](#abh_posts)
[Koray Tuğberk GÜBÜR](https://www.holisticseo.digital)Owner and Founder at Holistic SEO & DigitalKoray Tuğberk GÜBÜR is the CEO and Founder of Holistic SEO & Digital where he provides SEO Consultancy, Web Development, Data Science, Web Design, and Search Engine Optimization services with strategic leadership for the agency’s SEO Client Projects. Koray Tuğberk GÜBÜR performs SEO A/B Tests regularly to understand the Google, Microsoft Bing, and Yandex like search engines’ algorithms, and internal agenda. Koray uses Data Science to understand the custom click curves and baby search engine algorithms’ decision trees. Tuğberk used many websites for writing different SEO Case Studies. He published more than 10 SEO Case Studies with 20+ websites to explain the search engines. Koray Tuğberk started his SEO Career in 2015 in the casino industry and moved into the white-hat SEO industry. Koray worked with more than 700 companies for their SEO Projects since 2015. Koray used SEO to improve the user experience, and conversion rate along with brand awareness of the online businesses from different verticals such as retail, e-commerce, affiliate, and b2b, or b2c websites. He enjoys examining websites, algorithms, and search engines. Latest posts by Koray Tuğberk GÜBÜR ([see all](https://www.holisticseo.digital/author/koray-tugberk-gubur/))

- [Sliding Window](https://www.holisticseo.digital/theoretical-seo/sliding-window-technique-and-algorithm/) - August 12, 2024
- [B2P Marketing: How it Works, Benefits, and Strategies](https://www.holisticseo.digital/marketing/b2p-marketing/) - April 26, 2024
- [SEO for Casino Websites: A SEO Case Study for the Bet and Gamble Industry](https://www.holisticseo.digital/marketing/seo-for-casino-websites-a-seo-case-study-for-bet-and-gamble-industry/) - February 5, 2024