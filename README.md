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



FaceNet is a siamese network architecture developed by Google in 2015. They use a deep CNN to directly optimize the embedding itself, rather than an intermediate bottleneck layer as seen in previous approaches.for a given anchor image a, they use triplets that violate the triplet constraint, by selecting the inputs p and n such that d(a, p) is maximized, and d(a, n) is minimized.


