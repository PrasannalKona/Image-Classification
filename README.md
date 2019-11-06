# Image-Classification
using TensorFlow



The user can upload any flower picture in the flower_photos folder. The model will detect what kind of flower the image contains. The model is trained only for daisies, dandelions, roses, sunflowers, tulips.


# Steps to perform
1. sudo pip3 install — ignore-installed — upgrade tensorflow
2. pip3 install tensorflow-hub
3. python3 retrain.py --bottleneck_dir=bottlenecks --how_many_training_steps 500 --model_dir=inception --output_graph=retrained_graph.pb --output_labels=retrained_labels.txt --image_dir flower_photos/
4. python3 label_image.py — graph=retrained_graph.pb — image=test_images/rose.jpg — labels=retrained_labels.txt — output_layer=final_result — input_layer=Placeholder


#Output

roses 0.90414816
sunflowers 0.040658467
daisy 0.025798427
tulips 0.018112848
dandelion 0.011282069
