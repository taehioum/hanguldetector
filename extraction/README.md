# Feature Extraction from a given font image

This is a very crude algorithm, that kinda works.

Drawbacks:
The composition of border boxes of a same character can differ,
if the font is different.


One possible solution would be to extract the outermost border.
However, this means that we can only get 4 values(if we normalize) per
character, and this is not enough to distinguish characters.

One other solution would be to use the outermost border, but use a different
normalizing strategy, that gives more than 4 numbers.

# file description

* main.py: execution code
* features.py: extract features from hangeul character images
* generate\_date.py: generate dataset.npy from a selection of fonts
* score.py: calculate scores for each feature

#TODO
get a better normalization technique for font profiles, that increases
accuracy.