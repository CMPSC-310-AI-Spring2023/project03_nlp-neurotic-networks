# Report by Jeff & Aidan

## Data

TODO: Describe the data used in your project and how you obtained it. Cite (provide a link to) any sources you have used.

## Text Generation

We followed the instructor provided tutorial [here, on Tensorflow](https://www.tensorflow.org/text/tutorials/text_generation#build_the_model), making some adjustments where necessary. Those adjustments include (but aren't limited to) tweaking the process of collecting the input file, *heavily* increasing the number of training epochs, and adjusting the starting characters when creating a new prediction.

```
The story takes place in the future where the greenhouse gases have caused the polar icecaps to melt, with the rest of the robot childs and gives him the bad news that his estimate of years is now down to days before hereve codes with the apsears in video clips behind the black hole Gquan't stand till be a trap.
```

```
MODIFIED VERSION:
The story takes place in the future where the greenhouse gases have caused the polar icecaps to melt. The robot children give the bad news that the estimate of years is now down to days before the code will appear in video clips to make the black hole a trap.
```

## Supplemental Production

The supplemental production was created through the use of DALL-E. We asked for a movie poster for a movie about a climate disaster brought about by robot children. The stark yellow-and-black coloring and the pictured barren wasteland definitely convey the feeling we were hoping to see. The looming robot hand in the corner of the poster is a particularly nice touch.

![Movie Poster](movie-poster.png "Movie Poster")


## Analysis

Our generated text is *much* better than our initial attempt. We initially used subtitle files from 11 different movies, and the resulting text--no matter how much we tweaked the number of epochs--was always incoherent, probably because the contents of those 11 movies varied *drastically* (compare the dialogue, or lack thereof, in *WALL-E* to something like *Soylent Green*). We pivoted and went with synopsis files for the same 11 movies, hoping that more similarly structured content would help keep some semblance of consistency and coherence in the generated text.

This was a *major* improvement, but only after *severely* cranking up the number of training epochs. Since the input text was much, *much* smaller, we had to iterate through the training process over 100 times more to achieve results that were satisfactory and showed losses similar to the generation using the massive subtitle file.

## Carbon Footprint

TODO: Reflect on carbon footprint of your text generation implementation. Consider ethical implications of this type of work.

## Challenges and Learning Experiences

TODO: Discuss any challenges you have encountered during the work on this lab and describe what have you learned.
