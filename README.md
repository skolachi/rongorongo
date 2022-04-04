# rongorongo
Language Modeling for the Rongorongo script


3/04/2022: Created repo based on older code to do an analysis of Rongorongo script found in Easter Islands

The script is considered undeciphered although several claims of decipherment have been made. 

Corpus of the script can be found here- http://kohaumotu.org/rongorongo_org/concord/index.html

About the transliteration system (Barthel system)- http://kohaumotu.org/rongorongo_org/corpus/codes.html

http://kohaumotu.org/rongorongo_org/corpus/extended.html

Notes: 

1. One of the complexities is that it is unclear if Rongorongo is a linear left-to-right script. There are different ways to conjoin signs - concatenation, linking, stacking and merging (http://kohaumotu.org/rongorongo_org/corpus/combine.html). How do you extract sign sequence for these different kinds of punctuations? Left-to-right order is assumed to be default but obviously does not have to be. 

2. Signs can have affixes which we ignore for now. 

3. Signs can also be worn out and they are indicated in parenthesis. I followed the notes on the transliteration pages linked above to extract sign sequence in such examples. 

4. If a sign is followed by an exclamation mark, it's yet to be definitely identified. A question mark indicates doubtful identification.

This Colab Jupyter notebook trains a BERT style Masked language model using inscriptions which do not contain any unidentified (!) or doubtful (?) signs.

Statistics- 

| Type  | Number of examples |
| ------------- | ------------- |
| All inscriptions | 14653 |
| Fully identified inscriptions | 7441 |
| Inscriptions with missing or doubtful symbols | 7212 |

Fully identified inscriptions were used as training dataset. The Masked Language model can be used to fill missing and confirm doubtful signs. 

For the baseline model, I used some default parameters. Hyperparameter tuning is required to find the best model parameters.

There is a sparsity issue in the distribution of signs. Check the frequency distribution bar plot in the notebook. 


