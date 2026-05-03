<h2>TensorFlow-FlexUNet-Image-Segmentation-Combined-Breast-Cancer-Ultrasound (2026/05/03)</h2>

This is the first experiment of Image Segmentation for Combined Breast Cancer Ultrasound (Benign and Malignant)
 based on 
our <a href="./src/TensorFlowFlexUNet.py">TensorFlowFlexUNet</a>
 (<b>TensorFlow Flexible UNet Image Segmentation Model for Multiclass</b>) and a 512x512 pixels PNG 
 <a href="https://drive.google.com/file/d/1ldE__nA49tKg8Kqaz_vHIvku34LMzr2O/view?usp=sharing">
Augmented-Combined-Breast-Cancer-Ultrasound-ImageMask-Dataset.zip</a> with colorized masks (<a href="https://creativecommons.org/publicdomain/zero/1.0/">
CC0: Public Domain</a>), which was derived by us from 
<br><br>
<a href="https://www.kaggle.com/datasets/omarsherifrabie/combined-breast-cancer-ultrasound-dataset">
<b>Combined Breast Cancer Ultrasound Dataset</b>
</a>.
<br><br>
<hr>
<b>Actual Image Segmentation for Breast Cancer Ultrasound of 512x512 pixels</b><br>
As shown below, the inferred masks look similar to the ground truth masks. <br>
<br>
<b>class-color-map = {Benign:green, Malignant: red}</b><br>
<br>
<table>
<tr>
<th>Input: image</th>
<th>Mask (ground_truth)</th>
<th>Prediction: inferred_mask</th>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test/images/10009.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test/masks/10009.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test_output/10009.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test/images/10291.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test/masks/10291.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test_output/10291.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test/images/10484.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test/masks/10484.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test_output/10484.png" width="320" height="auto"></td>
</tr>
</table>
<hr>
<br>
<h3>1. Dataset Citation</h3>
The dataset used here has been taken from the following kaggle web site:<br><br>
<a href="https://www.kaggle.com/datasets/omarsherifrabie/combined-breast-cancer-ultrasound-dataset">
<b>Combined Breast Cancer Ultrasound Dataset</b>
</a> on the kaggle.com.
<br><br>
The following explanation was taken from the above kaggle web site.
<br><br>
<b>About Dataset</b><br>
We use a merger of two major benchmark datasets for Breast Ultrasound Image Segmentation; <br><br>
<a href="https://www.cancerimagingarchive.net/collection/breast-lesions-usg/">
<b>Breast- Lesions-USG dataset from the Cancer Imaging Archive</b></a>, and <br>
<a href="https://data.mendeley.com/datasets/7fvgj4jsp7/1"><b>BUS-UCLM: Breast ultrasound lesion segmentation dataset</b></a>. <br>
<br>The former contains 256 ultrasound grayscale-alpha images, each accompanied with a mask image covering the malignant tumors in addition to a mask image covering benign tumor area in the image. The dataset is imbalanced, since there are only 14 images containing suspicious regions and only 4 images with no tumor at all. The images are formatted as PNG files, stored as RGBA despite the absence of color in the images. The latter dataset contains 683 images, formatted the same as the former. Consisting of 174 benign tumors, 90 malignant tumors, and 419 normal images, combining these two datasets creates a dataset with 939 total images, 423 containing no tumor, 188 containing benign tumors, and 328 containing malignant tumors. In addition to increasing the dataset size, 
this makes the dataset more balanced and diverse, which is a common problem in image segmentation problems.
<br><br>
<b>License</b><br>
<a href="https://creativecommons.org/publicdomain/zero/1.0/">
CC0: Public Domain
</a>
<br>
<br>
<h3>
<a id="2">
2 Combined Breast Cancer Ultrasound ImageMask Dataset
</a>
</h3>
 If you would like to train this Breast-Ultrasound-Images Segmentation model by yourself,
 please download the dataset from the google drive  
 <a href="https://drive.google.com/file/d/1ldE__nA49tKg8Kqaz_vHIvku34LMzr2O/view?usp=sharing">
Augmented-Combined-Breast-Cancer-Ultrasound-ImageMask-Dataset.zip</a> (<a href="https://creativecommons.org/publicdomain/zero/1.0/">
CC0: Public Domain</a>)
, expand the downloaded ImageMaskDataset and put it under <b>./dataset</b> folder to be
<br>
<pre>
./dataset
└─Combined-Breast-Cancer-Ultrasound
    ├─test
    │   ├─images
    │   └─masks
    ├─train
    │   ├─images
    │   └─masks
    └─valid
        ├─images
        └─masks
</pre>
<br>
<b>Combined Breast Cancer Ultrasound Statistics</b><br>
<img src ="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/Combined-Breast-Cancer-Ultrasound_Statistics.png" width="512" height="auto"><br>
<br>
As shown above, the number of images of train and valid datasets is not so large to use for the
 training set of our segmentation model.
<br>
<br>
<b>Train_images_sample</b><br>
<img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/asset/train_images_sample.png" width="1024" height="auto">
<br>
<b>Train_masks_sample</b><br>
<img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/asset/train_masks_sample.png" width="1024" height="auto">
<br>

<h3>
3 Train TensorFlowFlexUNet Model
</h3>
 We trained Breast-Ultrasound-Images TensorFlowFlexUNet Model by using the following
<a href="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/train_eval_infer.config"> <b>train_eval_infer.config</b></a> file. <br>
Please move to ./projects/TensorFlowFlexUNet/Breast-Ultrasound-Images and run the following bat file.<br>
<pre>
>1.train.bat
</pre>
, which simply runs the following command.<br>
<pre>
>python ../../../src/TensorFlowFlexUNetTrainer.py ./train_eval_infer.config
</pre>
<hr>

<b>Model parameters</b><br>
Defined a small <b>base_filters = 16 </b> and large <b>base_kernels = (11,11)</b> for the first Conv Layer of Encoder Block of 
<a href="./src/TensorFlowFlexUNet.py">TensorFlowFlexUNet.py</a> 
and a large <b>num_layers = 8</b> (including a bridge between Encoder and Decoder Blocks).
<pre>
[model]
;You may specify your own UNet class derived from our TensorFlowFlexModel
model         = "TensorFlowFlexUNet"
generator     =  False
image_width    = 512
image_height   = 512
image_channels = 3
num_classes    = 3

base_filters   = 16
base_kernels   = (11,11)
num_layers     = 8
dropout_rate   = 0.04
dilation       = (1,1)
</pre>
<b>Learning rate</b><br>
Defined a small learning rate.  
<pre>
[model]
learning_rate  = 0.00007
</pre>
<b>Loss and metrics functions</b><br>
Specified "categorical_crossentropy" and <a href="./src/dice_coef_multiclass.py">"dice_coef_multiclass"</a>.<br>
<pre>
[model]
loss           = "categorical_crossentropy"
metrics        = ["dice_coef_multiclass"]
</pre>
<b>Dataset class</b><br>
Specifed <a href="./src/ImageCategorizedMaskDataset.py">ImageCategorizedMaskDataset</a> class.<br>
<pre>
[dataset]
class_name    = "ImageCategorizedMaskDataset"
</pre>
<br>
<b>Learning rate reducer callback</b><br>
Enabled learing_rate_reducer callback, and a small reducer_patience.
<pre> 
[train]
learning_rate_reducer = True
reducer_factor     = 0.4
reducer_patience   = 4
</pre>
<b>Early stopping callback</b><br>
Enabled early stopping callback with patience parameter.
<pre>
[train]
patience      = 10
</pre>

<b>RGB Color map</b><br>
Specifed rgb color map dict for Breast-Ultrasound-Images 3 classes.<br>
<pre>
[mask]
mask_datatype= "categorized"
mask_file_format = ".png"
;Breast-Ultrasound-Images rgb color map dict for 1+2 classes.
;        background:black , Benign:green  Malignant: red
rgb_map = {(0,0,0):0,(0,255,0):1, (255,0,0):2 }
</pre>

<b>Epoch change inference callback</b><br>
Enabled <a href="./src/EpochChangeInferencer.py">epoch_change_infer callback</a></b>.<br>
<pre>
[train]
epoch_change_infer       = True
epoch_change_infer_dir   =  "./epoch_change_infer"
num_infer_images         = 6
</pre>

By using this callback, on every epoch_change, the inference procedure can be called
 for 6 images in <b>mini_test</b> folder. This will help you confirm how the predicted mask changes 
 at each epoch during your training process.<br> 
<br> 
As shown below, early in the model training, the predicted masks from our UNet segmentation model showed 
discouraging results.
 However, as training progressed through the epochs, the predictions gradually improved. 
 <br> 
<br>
<b>Epoch_change_inference output at starting (epoch 1,2,3)</b><br>
<img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/asset/epoch_change_infer_at_start.png" width="1024" height="auto"><br>
<br>
<b>Epoch_change_inference output at middlepoint (epoch 23,24,25)</b><br>
<img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/asset/epoch_change_infer_at_middle.png" width="1024" height="auto"><br>
<br>

<b>Epoch_change_inference output at ending (epoch 48,49,50)</b><br>
<img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/asset/epoch_change_infer_at_end.png" width="1024" height="auto"><br>
<br>

In this experiment, the training process was terminated at epoch 50.<br><br>
<img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/asset/train_console_output_at_epoch50.png" width="920" height="auto"><br>
<br>

<a href="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/eval/train_metrics.csv">train_metrics.csv</a><br>
<img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/eval/train_metrics.png" width="520" height="auto"><br>

<br>
<a href="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/eval/train_losses.csv">train_losses.csv</a><br>
<img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/eval/train_losses.png" width="520" height="auto"><br>

<br>

<h3>
4 Evaluation
</h3>
Please move to <b>./projects/TensorFlowFlexUNet/Breast-Ultrasound-Images</b> folder,<br>
and run the following bat file to evaluate TensorFlowUNet model for Breast-Ultrasound-Images.<br>
<pre>
./2.evaluate.bat
</pre>
This bat file simply runs the following command.
<pre>
python ../../../src/TensorFlowFlexUNetEvaluator.py ./train_eval_infer_aug.config
</pre>

Evaluation console output:<br>
<img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/asset/evaluate_console_output_at_epoch50.png" width="920" height="auto">
<br><br>Image-Segmentation-Breast-Ultrasound-Images

<a href="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/evaluation.csv">evaluation.csv</a><br>
The loss (categorical_crossentropy) to this Breast-Ultrasound-Images/test was low, and dice_coef_multiclass 
high as shown below.
<br>
<pre>
categorical_crossentropy,0.0171
dice_coef_multiclass,0.9914
</pre>
<br>

<h3>
5 Inference
</h3>
Please move to a <b>./projects/TensorFlowFlexUNet/Breast-Ultrasound-Images</b> folder<br>
,and run the following bat file to infer segmentation regions for images by the Trained-TensorFlowUNet model for Breast-Ultrasound-Images.<br>
<pre>
./3.infer.bat
</pre>
This simply runs the following command.
<pre>
python ../../../src/TensorFlowFlexUNetInferencer.py ./train_eval_infer_aug.config
</pre>
<hr>
<b>mini_test_images</b><br>
<img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/asset/mini_test_images.png" width="1024" height="auto"><br>
<b>mini_test_mask(ground_truth)</b><br>
<img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/asset/mini_test_masks.png" width="1024" height="auto"><br>

<hr>
<b>Inferred test masks</b><br>
<img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/asset/mini_test_output.png" width="1024" height="auto"><br>
<br>
<hr>
<b>Enlarged images and masks for Breast Cancer Ultrasound of 512x512 pixels</b><br>
<br>
<b>class-color-map = {Benign:green, Malignant: red}</b><br>
<br>
<table>
<tr>
<th>Image</th>
<th>Mask (ground_truth)</th>
<th>Inferred-mask</th>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test/images/10013.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test/masks/10013.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test_output/10013.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test/images/10069.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test/masks/10069.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test_output/10069.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test/images/10437.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test/masks/10437.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test_output/10437.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test/images/10291.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test/masks/10291.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test_output/10291.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test/images/10388.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test/masks/10388.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test_output/10388.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test/images/10678.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test/masks/10678.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Combined-Breast-Cancer-Ultrasound/mini_test_output/10678.png" width="320" height="auto"></td>
</tr>
</table>
<hr>
<br>
<h3>
References
</h3>
<b>1. Breast Ultrasound Images Dataset</b><br>
<a href="https://www.kaggle.com/datasets/aryashah2k/breast-ultrasound-images-dataset">
https://www.kaggle.com/datasets/aryashah2k/breast-ultrasound-images-dataset
</a>
<br>
<br>
<b>2. Breast lesion detection using an anchor-free network from ultrasound images with segmentation-based enhancement</b><br>
Yu Wang & Yudong Yao<br>
<a href="https://www.nature.com/articles/s41598-022-18747-y">
https://www.nature.com/articles/s41598-022-18747-y
</a>
<br>
<br>
<b>3. Classification of Breast Cancer Ultrasound Images with Deep Learning-Based Models </b><br>
Fatih Uysa,and Mehmet Murat Köse<br>
<a href="https://www.mdpi.com/2673-4591/31/1/8/html">
https://www.mdpi.com/2673-4591/31/1/8/html
</a>
<br>
<br>
<b>4. A CNN Deep Learning Technique for Prediction of Breast Cancer using Ultrasound Image
</b><br>
Atisham Khan and Silky Pareyani<br>
<a href="https://www.jetir.org/papers/JETIR2303813.pdf">
https://www.jetir.org/papers/JETIR2303813.pdf
</a>
<br>
<br>
<b>5. Discrimination of Breast Cancer Based on Ultrasound Images and Convolutional Neural Network
</b><br>
Rui Du,Yanwei Chen,Tao Li, Liang Shi,Zhengdong Fei,and Yuefeng Li
<br>
<a href="https://www.hindawi.com/journals/jo/2022/7733583/">
https://www.hindawi.com/journals/jo/2022/7733583/
</a>
<br>
<br>
<b>6. TensorFlow-FlexUNet-Image-Segmentation-BUS-BRA</b><br>
Toshiyuki Arai<br>
<a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-BUS-BRA">
https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-BUS-BRA</a>
<br>
<br>
<b>7. TensorFlow-FlexUNet-Image-Segmentation-BUS-UC</b><br>
Toshiyuki Arai<br>
<a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-BUS-UC">
https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-BUS-UC</a>
<br>
<br>
<b>8. TensorFlow-FlexUNet-Image-Segmentation-BUS-UCLM</b><br>
Toshiyuki Arai<br>
<a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-BUS-UCLM">
https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-BUS-UCLM
</a>
<br><br>
<b>9. TensorFlow-FlexUNet-Image-Segmentation-BUSI-WHU-Breast-Cancer</b><br>
Toshiyuki Arai<br>
<a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-BUSI-WHU-Breast-Cancer">
https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-BUSI-WHU-Breast-Cancer
</a>
<br><br>
