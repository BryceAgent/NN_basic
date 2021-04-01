# NN_basic

Just a neural network I wrote based on the "recipe" provided by Michael Nielsen here http://neuralnetworksanddeeplearning.com/chap1.html

The neural network identifies handwritten digits from the MNist dataset that I downloaded from here https://github.com/mnielsen/rmnist/blob/master/data/mnist.pkl.gz

I adapted certain elements of my neural network that differ in important ways from the original recipe. For example, the original used cPickle and gzip to decompress and organize the dataset, but I decompressed the dataset outside of the NN program and fed it in as a csv. I also used the pandas library, as that seems to be the standard in data science for organizing datasets. This required several important modifications in how the data was loaded and acted on at various points in the program.

Another important difference is that I wrote the entire program in a single file. This is probably not ideal for a larger project but for understanding the ins and outs of a single, basic NN it made it easier to see and find how parts of the program were working (or not). Otherwise, the function is practically identical with that of the recipe I used and linked above. 

I also wrote in a couple lines to save the NN structure I used on a given training session and record its highest accuracy and the weights/biases values that gave that result. Examples of my results can be found in the wb_save.txt file.

The best accuracy I was able to achieve was 86%. From what I have learned I believe that adapting the learning rate during training, such as by using the Adam optimizer or something like it, would allow the program to better hone in on "narrow" but "deep" values of the gradient descent space. Overall, for it being the first neural network I've written by myself with no help or guidance apart from the written tutorial linked above, I'm satisfied by the performance I achieved.

The program as written can be run provided the appropriate dataset is used. The values for 'net', 'epochs', and 'learning_rate' can be changed to find different results. From my tinkering with the model, two hidden layers seems to achieve the best results.
