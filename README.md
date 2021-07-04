## Steps
<br />
<b>Step 1.</b> Clone:
git clone https://github.com/iniTugasAkhir/TFOD
<br/><br/>
<b>Step 2.</b> Create a new virtual environment 
<pre>
python -m venv objectDetection
</pre> 
<br/>
<b>Step 3.</b> Activate your virtual environment
<pre>
.\objectDetection\Scripts\activate 
</pre>
<br/>
<b>Step 4.</b> Install dependencies and add virtual environment to the Python Kernel
<pre>
python -m pip install --upgrade pip
pip install ipykernel
python -m ipykernel install --user --name=objectDetectionL
</pre>
<br/>
Run Jupyter Notebook
<pre>
jupyter notebook
<pre/>
<br/>
<b>Step 5.</b> Collect images using the Notebook <a href="https://github.com/iniTugasAkhir/TFOD/blob/main/1.%20Image%20Collection.ipynb">1. Image Collection.ipynb</a>
<br/>
<b>Step 6.</b> Manually divide collected images into two folders train and test. So now all folders and annotations should be split between the following two folders. <br/>
\iniTugasAkhir\Tensorflow\workspace\images\train<br />
\iniTugasAkhir\Tensorflow\workspace\images\test
<br/><br/>
<b>Step 7.</b> Begin training process by opening <a href="https://github.com/iniTugasAkhir/TFOD/blob/main/2.%20Training%20and%20Detection.ipynb">2. Training and Detection.ipynb</a>, this notebook will walk you through installing Tensorflow Object Detection, making detections, saving and exporting your model. 
<br /><br/>
<b>Step 8.</b> During this process the Notebook will install Tensorflow Object Detection. You should ideally receive a notification indicating that the API has installed successfully at Step 8 with the last line stating OK.  
If not, resolve installation errors by referring to the <a href="https://github.com/iniTugasAkhir/TFODCourse/blob/main/README.md">Error Guide.md</a> in this folder.
<br /> <br/>
<b>Step 9.</b> Once you get to step 6. Train the model, inside of the notebook, you may choose to train the model from within the notebook. I have noticed however that training inside of a separate terminal on a Windows machine you're able to display live loss metrics. 
<br />
<b>Step 10.</b> You can optionally evaluate your model inside of Tensorboard. Once the model has been trained and you have run the evaluation command under Step 7. Navigate to the evaluation folder for your trained model e.g. 
<pre> cd Tensorlfow/workspace/models/my_ssd_mobnet/eval</pre> 
and open Tensorboard with the following command
<pre>tensorboard --logdir=. </pre>
Tensorboard will be accessible through your browser and you will be able to see metrics including mAP - mean Average Precision, and Recall.
<br />
