# Machine Learning

### Machine Learning 

: Field of study that gives computers the ability to learn without being explicitly programmed - Arthur Samuel 



- **Supervised learning** : learning with labeled examples - training set / 이미 정해진 데이터로 학습

  ex ) 강아지, 고양이 등의 사진을 모아서 학습시킨다. 

- **Unsupervised learning** : un-labeled data

  ex ) Google news grouping , Word clustering 



- Training data set 

  x = [3, 6, 9] -> y = 3 이러한 데이터가 있을 때, 컴퓨터에게 x = [9, 6, 3] 데이터를 입력했을 때, y = 3 임을 아는 것. 

  여기서 x, y, 즉, 학습시키는데 사용된 데이터가 training data set 

  

- Types of supervised learning 

  - **Regression** 

    ex ) Predicting final exam score based on time spent

  - **binary classification**

    ex ) Pass / Non-pass based on time spent

  - **multi-label classification**

    ex ) Letter grade (A, B, C, E and F) based on time spent

    

### Tensorflow 

: is an open source software library for numerical computation using data flow graphs.



```python
import tensorflow as tf
hello = tf.constant("Hello, Tensorflow!")
sess = tf.Session()
print(sess.run(hello))

node1 = tf.constant(3.0, tf.float32)
node2 = tf.constant(4.0)
node3 = tf.add(node1, node2)

# 이렇게 출력하면 tensor를 출력하는 것 
print(node1, node2, node3)

sess = tf.Session()
print("sess.run(node1, node2) :", sess.run([node1, node2]))
print("sess.run(node3) : ", sess.run(node3) )
```

1) Build graph using TensorFlow operations

2) feed data and run graph (operation) - sess.run(op)

3) update variables in the graph



```python
# placeholder - node인데 미리 graph를 만들고 값을 넘겨준다고 생각하면 된다. 

a = tf.placeholder(tf.float32)
b = tf.placeholder(tf.float32)
adder_node = a + b

print(sess.run(adder_node, feed_dict={a: 3, b: 4.5}))
print(sess.run(adder_node, feed_dict={a: [1, 3], b: [2, 4]}))
```





