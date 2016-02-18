# SerbMR - The Serbian Movie Review Dataset
The Serbian Movie Review Dataset collection consists of three movie review datasets in Serbian which were constructed for the task of sentiment analysis:
* [Collected movie reviews in Serbian](https://github.com/vukbatanovic/SerbMR/releases/download/v1.0/Collected_Movie_Reviews_in_Serbian.zip)
* [SerbMR-2C - The Serbian Movie Review Dataset (2 Classes)](https://github.com/vukbatanovic/SerbMR/releases/download/v1.0/SerbMR-2C.arff)
* [SerbMR-3C - The Serbian Movie Review Dataset (3 Classes)](https://github.com/vukbatanovic/SerbMR/releases/download/v1.0/SerbMR-3C.arff)


## Collected movie reviews in Serbian
This is a collection of 4725 movie reviews in Serbian.

### Data sources
Reviews were gathered from the following eight websites:
* 2kokice.com
* filmskerecenzije.com
* filmskihitovi.blogspot.com
* happynovisad.com
* kakavfilm.com
* mislitemojomglavom.blogspot.com
* popboks.com
* yc.rs

This corpus contains the reviews published on these websites from their inception until 01/01/2015.
Some of the reviews are written in Cyrillic, but most of them are in the Latin script.
A great majority of the reviews are in the Ekavian pronunciation.

### Scoring systems
A 1-10 scoring system was adopted as the standard, since most websites use it.
A 1-5 scoring system, used on happynovisad.com and yc.rs, was translated to 1-10 by multiplying the original scores by two.
For these websites a plus/minus next to the original score was treated as an increment/decrement of the translated score.
Pluses/minuses in the 1-10 scoring systems were ignored and X.5 scores were rounded down to X.
In a few rare instances where a zero score was given, it was translated into a score of one.

### Score distribution
This dataset is skewed towards the positive reviews - if scores 1-4 are treated as negative, 5-6 as neutral, and 7-10 as positive, the corpus contains 841 negative, 1278 neutral, and 2606 positive reviews.

### Subsets
The SerbMR-2C/SerbMR-3C datasets are two-class/three-class balanced subsets of this collection.

### Format
The reviews are presented as individual UTF-8-encoded TXT files sorted into folders according to their source website and their score.
File names are mostly given according to movie titles (and sometimes the release year).
However, for three of the source websites (happynovisad.com, kakavfilm.com, popboks.com) a different naming scheme was used, based on a unique ID number for each movie review.


## SerbMR-2C
This two-class balanced sentiment analysis dataset contains 1682 movie reviews in Serbian (841 positive and 841 negative reviews).
A great majority of the reviews are in the Ekavian pronunciation.

### Relation to other datasets
SerbMR-2C is a subset of the imbalanced "Collected Movie Reviews in Serbian" dataset and was constructed by including all 841 negative reviews from it and choosing 841 positive reviews in the manner described in the reference paper.
The balancing procedure minimizes the non-sentiment-related differences between the classes and takes into account review scores, review lengths and the differences in writing styles used on different source websites.

SerbMR-2C is also a subset of the SerbMR-3C dataset as it contains the positive/negative reviews from that dataset, but not the neutral ones.

### Format
The dataset is formatted as a Weka .arff file, with one review per line.
All Cyrillic reviews were converted into the Latin script.


## SerbMR-3C
This three-class balanced sentiment analysis dataset contains 2523 movie reviews in Serbian (841 positive, 841 neutral, and 841 negative reviews).
A great majority of the reviews are in the Ekavian pronunciation.

### Relation to other datasets
SerbMR-3C is a subset of the imbalanced "Collected Movie Reviews in Serbian" dataset and was constructed by including all 841 negative reviews from it and choosing 841 positive and 841 neutral reviews in the manner described in the reference paper.
The balancing procedure minimizes the non-sentiment-related differences between the classes and takes into account review scores, review lengths and the differences in writing styles used on different source websites.

SerbMR-3C is also a superset of the SerbMR-2C dataset as it contains all of the positive/negative reviews from that dataset, as well as the additional 841 neutral reviews.

### Format
The dataset is formatted as a Weka .arff file, with one review per line.
All Cyrillic reviews were converted into the Latin script.


## Reference
If you wish to use these datasets in your paper or project, please cite:

**Reliable Baselines for Sentiment Analysis in Resource-Limited Languages: The Serbian Movie Review Dataset**, Vuk Batanović, Boško Nikolić, Milan Milosavljević, in Proceedings of the 10th International Conference on Language Resources and Evaluation (LREC 2016), Portorož, Slovenia (2016).

## License
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](http://creativecommons.org/licenses/by-nc-sa/4.0/)

If you wish to use these datasets in a commercial product, please contact me at: bv115045p / at / student.etf.bg.ac.rs

