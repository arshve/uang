# Money Clasification Using Docker and Inception V3

Train Image Data

```
python tensorflow/tensorflow/examples/image_retraining/retrain.py \
--bottleneck_dir=/bottlenecks \
--model_dir=/inception \
--output_labels=/retrained_labels.txt \
--output_graph=/retrained_graph.pb \
--image_dir=/training_images/
```

Predict Test Image

```
python tensorflow/tensorflow/examples/image_retraining/label_image.py \
--graph=/retrained_graph.pb \
--labels=/retrained_labels.txt \
--image=/test_image.jpeg 
```
