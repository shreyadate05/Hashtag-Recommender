# Hashtag Recommender

```
Authors: Shivani Birmal, Shreya Date
```
- **Project title**
    Hashtag recommendation based on emotions and objects in images
- **Datasets to be used**
    There are no data sets publicly available.
    We will generate the following data sets using web scraping.
    1. Download 100 images for each of the 50 emotions.
    2. Annotate the images (manually or by leveraging an existing code) for object detection.
    3. Extract 50 hashtags for every detected object and input emotion.

So basically, we would have a mapping of

(x, y) → (image, emotion) → Multi label classification

(x, y) → (image, object) → Multi label classification

(X, y) → (emotion & object, hashtags) → Not necessarily ML involved.

- **Project idea (this should be approximately two paragraphs)**
    Given an image, predict meaningful hashtags for it.
    1. Detect emotions in the image.
    2. Detect objects in an image.
    3. Combine the detected objects and emotions to predict meaningful hashtags for it.

```
Part 1: Emotion detection
```
1. We have a dataset which contains mapping of images to emotions. This can be used
    as a training set where emotions are dependent variables and images are
    independent variables. We plan to implement multi-label classification for this. One
    image can express emotions like happiness, joy, gratitude etc.
2. We also plan to use colors in an image to predict emotions. For example, if pink is the
    dominating color in an image, then relevant emotions would be love, romance, blush
    etc.

```
Part 2 : Object detection
```
1. For better hashtag predictions, detecting objects in an image along with the emotions
    would give better results. For example, if the emotion detected is happy, and the


```
object in an image is a girl, then a hashtag like #happygirlsaretheprettiest or
#happygirlsshinebrighter are more relevant.
```
2. So, for object detection, we have a data set of annotated images. By training on that
    data set, or by using pure image processing wherever applicable, we should be able
    to identify
       i. labels relevant to people → girl, boy, man, woman
ii. labels relevant to age → old, young, babies, teen. For example, an aged man
and teenage girl should be appropriately tagged as #fatherdaughter instead of
#friends or #bffs.
iii. labels to identify time of the day → For example, if it’s early morning, probably
tags like #meditation, #calmness etc. would make sense.

```
Part 3 :
So, from Part 1 and Part 2, we have the emotions, colors, objects and basic tone of an
image with us. From this information we can generate hashtags by
```
1. clubbing adjectives (which could be emotions) and nouns (objects)
2. getting relevant hashtags straight from online tools by providing it emotions and
    objects detected
3. Going forward, these generated hashtags for an emotion-object pair will be stored in
    a JSON file. The generated JSON file can be looked up while generating hashtags for
    images having similar/same to start with objects and emotions.
- **Software you will use or need to write**
1. Beautiful soup and selenium for web scraping
2. The usual python libraries like scikit, pandas, keras for classification
3. OpenCV for image processing
- **Papers to read. Include 1-3 relevant papers. You will probably want to read at least
one of them before submitting your proposal.**
1. https://cs.stanford.edu/people/karpathy/main.pdf
2. https://arxiv.org/pdf/1605.05054.pdf
3. https://pdfs.semanticscholar.org/1ae4/519b5a4bb05d640ad4660ffeb375d78099d9.
pdf?_ga=2.91400090.1889990691.1585009050-1582625259.
- **Teamate. Will you have a teamate? If so, whom? Maximum team size is two students.**
Yes, we will be working in a team. Shivani Birmal and I (Shreya Date) will be teammates.
- **What is your plan of work? What will each team member be doing?**


Data gathering and data set creation would be worked upon together. Since there are 3
clear parts to the project, we will distribute the first two parts amongst ourselves. The
third part, which is hashtag generation, will again be worked upon together.


