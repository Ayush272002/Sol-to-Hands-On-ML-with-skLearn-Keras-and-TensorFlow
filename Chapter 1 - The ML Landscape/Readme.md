## Main challenges of ML

- Insufficient Quantity of Training Data
- Nonrepresentative Training Data
- Poor-Quality Data
- Irrelevant Features
- Overfitting the Training Data
- Underfitting the Training Data

## Big Picture

- There are many different types of ML systems: supervised or not, batch
  or online, instance-based or model-based.
- In an ML project you gather data in a training set, and you feed the
  training set to a learning algorithm. If the algorithm is model-based, it
  tunes some parameters to fit the model to the training set (i.e., to make
  good predictions on the training set itself), and then hopefully it will be
  able to make good predictions on new cases as well. If the algorithm is
  instance-based, it just learns the examples by heart and generalizes to
  new instances by using a similarity measure to compare them to the
  learned instances.
- The system will not perform well if your training set is too small, or if
  the data is not representative, is noisy, or is polluted with irrelevant
  features (garbage in, garbage out). Lastly, your model needs to be
  neither too simple (in which case it will underfit) nor too complex (in
  which case it will overfit).

## Tesing and Validation

- The only way to know how well a model will generalize to new cases is to
  actually try it out on new cases. One way to do that is to put your model in
  production and monitor how well it performs.
- A better option is to split your data into two sets: the training set and the test
  set. As these names imply, you train your model using the training set, and
  you test it using the test set. The error rate on new cases is called the
  generalization error (or out-of-sample error), and by evaluating your model
  on the test set, you get an estimate of this error. This value tells you how well
  your model will perform on instances it has never seen before.
