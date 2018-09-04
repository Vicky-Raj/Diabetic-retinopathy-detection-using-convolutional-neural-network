# Diabetic-retinopathy-detection-using-convolutional-neural-network

Diabetic retinopathy is medical condition where damage occurs in the retina due to diabetic mellitus.Diabetic retionapathy causes permanent blindnesss.Diabetic retionpathy can be diagnosed by looking at the fundus image of the eye.If the retina shows cotton wool spots we can be sure one is affectd by Diabetic retinopathy.

* Normal eye

![alt text](https://www.researchgate.net/profile/Andrzej_Grzybowski/publication/230588882/figure/fig4/AS:601678592086022@1520462763212/The-left-eye-fundus-after-treatment-The-retinal-vessels-abnormalities-returned-to_Q320.jpg)


* Cotton wool spots


![alt text](https://avclinic.com/wp-content/uploads/2016/05/Retinal-Signs-Cotton-wool-spot.jpg)


#### Model:
Due to the scarce nature of the dataset(85 images),it is infeasible to pre train a convolutional neural network from scratch.So the solution is to use transfer learning by fine tuning a VGG16 model trained on the imagenet datset.We can acheive this by freezing all the layers except the classifier and adding a custom softmax classifier and training it on the scarce dataset which allows the model to have maximum accuracy when predicting on new images.

Dataset used: http://www.it.lut.fi/project/imageret/diaretdb0/

* VGG16 model:


![alt text](https://qph.fs.quoracdn.net/main-qimg-83c7dee9e8b039c3ca27c8dd91cacbb4)



Trained model: https://drive.google.com/file/d/1T71PWUR3wwCuuvKR0TgdhCAuurqizInL/view

Fianl accuracy: 98.82%

