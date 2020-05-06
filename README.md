# deepfake-detection-image
This repository is based on xinyooo's deepfake-detection repository (https://github.com/xinyooo/deepfake-detection).<br> 
All credits to him. I've just tweaked the code to accept images and run the model so that it can predict an image instead of a video.

## Required folder structure -
In the current working directory, create a folder named as - 'dataset'. Inside this folder create two folders titled 'real' and 'fake'. This
is all that's required. The program shall create directories titled 'cropped' inside both fake and real where the faces get saved.

## Steps to use -
1) Run the capture_img notebook <br>
2) Run the deepfake_detection_train notebook (This will output a model file that gets saved in your cwd) <br>
3) Run the model_play notebook. Here, you'll have to change the path in the following line - <br>
   (Replace '19.png' with the path of the image you want to check)

```python
data = np.array(img_to_array(load_img('19.png')))
```

## Result
[0] denotes that the image was detected to be fake<br>
[1] denotes that the image was detected to be real
