# one-shot-recoginition
One-shot learning is a classification task where one, or a few, examples are used to classify many new examples in the future.

This characterizes tasks seen in the field of face recognition, such as face identification and face verification, where people must be classified correctly with different facial expressions, lighting conditions, accessories, and hairstyles given one or a few template photos.

Modern face recognition systems approach the problem of one-shot learning via face recognition by learning a rich low-dimensional feature representation, called a face embedding, that can be calculated for faces easily and compared for verification and identification tasks.

Very often, learning in siamese networks is done by the triplet loss function. Such models require three input images on training phase, and the loss is calculated as:
- Extract embeddings from an anchor input image a.
- Extract embeddings from a positive input image p (same class as the anchor).
- Extract embeddings from a negative input image n (different class from the anchor).
- Calculate the Euclidean distances d(a, p) and d(a, n). Ideally, the first distance should be as small as possible, while the latter should be as big as possible.
- The loss function is defined as: L = max(d(a, p)- d(a,n) + α, 0), where α is a parameter that defines how far away the dissimilarities should be, and enforces a distinction between the positive and the negative image.

Procedure to implement Siamese Neural Network (SNN) : <br>
1)Take an input and extract its embedding (mapping to a vector of continuous numbers) by passing it through a neural network. <br>
2)Repeat step 1 with a different input. <br>
3)Compare the two embeddings to check whether there is a similarity between the two data points. These two embeddings act as a latent feature representation of the data. In our case, images with the same person should have similar embeddings.

Very often, learning in siamese networks is done by the triplet loss function(contrastive loss/loss function dependent on distance). Such models require three input images on training phase, and the loss is calculated as:

1)Extract embeddings from an anchor input image a.

2)Extract embeddings from a positive input image p (same class as the anchor).

3)Extract embeddings from a negative input image n (different class from the anchor).

4)Calculate the Euclidean distances d(a, p) and d(a, n). Ideally, the first distance should be as small as possible, while the latter should be as big as possible.

5)The loss function is defined as: L = max(d(a, p)- d(a,n) + α, 0), where α is a parameter that defines how far away the dissimilarities should be, and enforces a distinction between the positive and the negative image.


#### References
https://www.coursera.org/lecture/convolutional-neural-networks/one-shot-learning-gjckG <br>
https://machinelearningmastery.com/one-shot-learning-with-siamese-networks-contrastive-and-triplet-loss-for-face-recognition/ <br>
https://heartbeat.fritz.ai/one-shot-learning-part-2-2-facial-recognition-using-a-siamese-network-5aee53196255 <br>
https://hub.packtpub.com/face-recognition-using-siamese-networks-tutorial/ <br>
https://blog.netcetera.com/face-recognition-using-one-shot-learning-a7cf2b91e96c  <br>
https://arxiv.org/abs/1503.03832 <br>
