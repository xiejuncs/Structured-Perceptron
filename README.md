Structured-Perceptron
=====================
README
Jun Xie (xie@eecs.oregonstate.edu)

Percpetron is a very efficient linear classification algorithm. The algorithm can be applied to non-structure data and structured data. At first, for non-structured data, we can use the traditional percpetron algorithm to train the model. There is one perceptron implementation with batch gradient descent method. I use the two gaussian dataset to test the algorithm. In order to run the algorithm, you just need to execute the following method and the final weight will be outputed in the screen.
        >> java Perceptron
In addition, for structured data, we need to extend the Perceptron algorithm. There is one variant of Perceptron called structured Perceptron. In order to run the algorithm, you just need to execute the following method and the final weight will be outputed in the screen. We use the NER dataset to train the model. If you want to train the model, you can compile the program and execute according to the following commands:
        >> javac *.java org/json/*.java -classpath "cloning-1.8.1-sources.jar:objenesis-1.2.jar:cloning-1.8.1.jar" -d classes -target 1.6
        // structured perceptron
        >> java -cp classes:.:cloning-1.8.1-sources.jar:objenesis-1.2.jar:cloning-1.8.1.jar NER ../data/train ../data/dev 1
        // structured perceptron with average, set the iteration number as 300, you can set the number in the AverageStructuredPerceptron.java
        >> java -cp classes:.:cloning-1.8.1-sources.jar:objenesis-1.2.jar:cloning-1.8.1.jar NER ../data/train ../data/dev 2
        The program will take for a while. Because I do not set the iteration number as the stopping criterion (for example 100). The stopping crition is to test whether the feature of gold sequence is equal to that of the predicted sequence.
        In addition, you can view the materials contained in the source file if you want to have a understanding of the algorithm and the whole landscrape of the structured prediction.

The source code is written by Java. If you have any question, please contact me. Thanks very much.
