# Waste-Classifier
Waste Classifier (optimized by Intel OpenVINO and Neural Compute Stick 2)

Link to data set: https://drive.google.com/file/d/1xNfhf6gwAeBb1xaQIdnw4lzAnnSIaPgT/view?usp=sharing

Important commands:
pip3 install tensorflow
python3 label_image.py --graph ./trained_model.pb --labels ./labels.txt --input_layer=Placeholder --output_layer final_result --image ./plastic_bottle.jpg
