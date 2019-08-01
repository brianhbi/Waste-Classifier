# Waste-Classifier
Waste Classifier (optimized by Intel OpenVINO and Neural Compute Stick 2)

Link to data set: https://drive.google.com/file/d/1xNfhf6gwAeBb1xaQIdnw4lzAnnSIaPgT/view?usp=sharing

**SETUP:**

Install OpenVINO: https://docs.openvinotoolkit.org/latest/_docs_install_guides_installing_openvino_linux.html (make sure NCS2 dependencies are installed!)

Install TensorFlow: pip3 install tensorflow

Navigate to Waste Classifier folder: 

python3 label_image.py --graph ./trained_model.pb --labels ./labels.txt --input_layer=Placeholder --output_layer final_result --image ./plastic_bottle.jpg

Establish your OPENVINO Environment Variables! 

Navigate to /$openvino installation dir$/deployment_tools/model_optimizer/: 

python3 mo_tf.py --input_model ./trained_model.pb --output_dir /home/"user"/ --input_shape (1,299,299,3) --mean_values (127.5,127.5,127.5) --scale 127.5

Navigate to inference engine/samples/python_samples/classifaction_sample_async: 

Plug in your NCS2 stick, run classification_sample_async.py and include the parameters "-d MYRIAD"!
