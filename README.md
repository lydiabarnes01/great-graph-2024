Data for the GREAT GRAPH COMPETITION 2024. 

### The Study

##### Contributors

Lydia Barnes

Alexandra Woolgar

Erin Goddard

##### Task

Participants viewed single images that were either greyscale or two-tone "Mooney" images. The bulk of the images were drawn from photos of real world objects, but a subset were synthetically generated to mimic the real images' low-level features (using [this](https://link.springer.com/article/10.1023/A:1026553619983) method). They could see each image for 33, 100, 300, or 900 ms before it was hidden behind a mask. They pressed a button to tell us whether they thought the image was of a real world object, or synthetically generated. 

You can see some stimuli under /img. The file ending "real_intact" is the greyscale version that we started with; "synth_intact" is a synthesised image with low-level statistics drawn from the real image; "real_mooney" is the real image converted to a two-tone image; and "synth_mooney" is the two-tone version of "synth_intact". And "mask-54.jpg" is a mask...

##### Research Question

Before people did this task, we showed them the greyscale versions of half of the two-tone images. We wanted to know whether people were better at judging whether the two-tone images were real or synthesised, when they had had time to peruse the greyscale version. If this "disambiguation" (clarifying what was in the two-tone images) helped people judge real from synthesised, we also wanted to know when they were able to use that information. If they saw a two-tone image for 100 ms, could they integrate what they'd learned from seeing the greyscale version into how they interpreted it?

We included greyscale images ("disambiguated", i.e. seen, or "control", i.e. new) in the timed task as a kind of baseline.

### The Data

##### subject

A unique ID for each subject.

##### exclude

Whether to exclude the participant. If exclude=FALSE, that person is a keeper. We flagged people exclude=TRUE if their accuracy in an easier, self-paced version of the task was too close to chance (<60%).

##### no_disambiguation_benefit

Whether this person benefitted from disambiguation in the easier, self-paced version of the task. Again, FALSE means that they're a keeper. 

We ran some pilot studies to check that people could use what they learned about a two-tone image from its greyscale version when they had unlimited time. (Generally, people got somewhat better at telling real from synthesised, and a lot better at saying what the real images were of.) So, we included the option here to only look at people who showed that benefit in self-paced trials, and test when that benefit emerged in our timed task with its 33:900 ms displays. 

##### duration

How long the image was on screen before the mask appeared, in milliseconds. Values are 33.33, 100, 300, and 900. 

##### block_type

Whether they're responding to "mooney" (two-tone) or "intact" (greyscale) images. It's called block type because we alternated between short blocks of two-tone and greyscale images. We tested people on a clump of two-tone images, then on the same images in greyscale, then moved on to another clump of two-tone images, and so on.

##### disambiguation

Whether this person saw this image in its greyscale form before they started the task. Options are "disambiguated" (seen) or "control" (unseen). People had seen all of the images in their two-tone form before, but only half in greyscale. If they saw an image in greyscale beforehand, they also had to label what they thought it was -- so they should have spent a good few seconds staring at and thinking about it. 

We've included this information for the "intact" blocks (when people were making real/synthesised judgements on greyscale images) so that we can see any effect of just seeing the same greyscale image multiple times. 

##### rt

Response time, from the onset of the response prompt screen to button press, in seconds. We don't expect this to be super informative, because we made people wait until after the mask before they could respond. 

##### dprime

Accuracy in d'. We use this because there were uneven numbers of real and synthesised images in the task -- so people who pressed "real" on every trial would usually be correct, but that would be a bad estimate of whether they could differentiate real from synthesised images. Instead, we take their hit rate (how often they respond "real" to a real image) and adjust it by their false alarm rate (how often they respond "real" to a synthesised image) to calculate their sensitivity, d'. A score below zero means they were consistently wrong. Above three means they were very sensitive to the difference between real and synthesised images. 

### The Design

The study was all within-subjects. Our key outcome (dependent variable) was d'. Predictors (independent variables) are duration and disambiguation. We care mainly about whether duration and disambiguation interact for the two-tone images, but you can also view this for the greyscale images for comparison.