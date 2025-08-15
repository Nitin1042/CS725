This is a very crude recommendation system that suggests songs based on input. This uses the GTZAN dataset. Please make sure to have the dataset or any other dataset that has songs before running the code. The input can be given by changing the path in the input_audio_file variable in the code.

We extract the following musical features:

MFCC - Mel Frequency Cepstral Coefficients: Represent the short-term power spectrum of sound. In layma terms it means it captures the texture of sound. Different instruments have different textures. This is used to identify the various instruments. Chroma Features: Summarize the energy distribution across the 12 pitch classes. Spectral Contrast: Measures the difference in amplitude between peaks and valleys in the audio spectrum. It means it captures the richness of the sound. Like whether it is has smooth ambience or heavy metal rock vibes. Tempo: Measure of the speed of the music. It measures the Beats per Minute. Using this features we project onto a feature space.

For a given input we also extract the features, project onto the feature space and measure the similarity by measuring the distance between the points.

We use the follwing distance measures:

Euclidean Distance
Manhattan Distance
Cosine Distance
Dynamic Time Warping
Once we measure all the distances, we give 5 songs for each distance measure whose distnaces are the lowest.
