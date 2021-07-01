# KNN-in-C
<h1>K Nearest Neighbours in C</h1>
<p>Introduction:-<br>
--</p>

<p>In pattern recognition, the k-nearest neighbors algorithm (k-NN) is a non-parametric method used for classification and regression. <br>
In both cases, the input consists of the k closest training examples in the feature space. The output depends on whether k-NN is used for classification or regression:</p>

<p> In k-NN classification, the output is a class membership. An object is classified by a majority vote of its neighbors, <br>
 with the object being assigned to the class most common among its k nearest neighbors (k is a positive integer, typically small). <br>
 If k = 1, then the object is simply assigned to the class of that single nearest neighbor.</p>

<p> In k-NN regression, the output is the property value for the object. <br>
 This value is the average of the values of its k nearest neighbors.</p>

<p>k-NN is a type of instance-based learning, or lazy learning, where the function is only approximated locally and all computation is deferred until classification. <br>
The k-NN algorithm is among the simplest of all machine learning algorithms.</p>

<p>Both for classification and regression, a useful technique can be to assign weight to the contributions of the neighbors, <br>
so that the nearer neighbors contribute more to the average than the more distant ones. For example, <br>
a common weighting scheme consists in giving each neighbor a weight of 1/d, where d is the distance to the neighbor.</p>

<p>The neighbors are taken from a set of objects for which the class (for k-NN classification) or the object property value (for k-NN regression) is known. <br>
This can be thought of as the training set for the algorithm, though no explicit training step is required.</p>

<p>A peculiarity of the k-NN algorithm is that it is sensitive to the local structure of the data.The algorithm is not to be confused with k-means, <br>
another popular machine learning technique.</p>

<p>Algorithm:-<br>
--<br>
Let m be the number of training data samples. Let p be an unknown point.</p>

<p> Store the training samples in an array of data points arr[]. This means each element of this array represents a tuple (x, y).</p>

<p> for i=0 to m:<br>
 Calculate Euclidean distance d(arr[i], p).</p>

<p> Make set S of K smallest distances obtained. Each of these distances correspond to an already classified data point.<br>
 Return the majority label among S.<br>
</p>

