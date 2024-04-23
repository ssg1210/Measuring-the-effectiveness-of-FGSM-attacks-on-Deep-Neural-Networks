# Measuring-the-effectiveness-of-FGSM-attacks-on-Deep-Neural-Networks
This project aims on measuring the effectiveness of fast gradient sign method attacks on Deep Neural Network s

The  fast  gradient  sign  method  uses  the  gradients  of  the  neural  network  to 
create  an  adversarial  example.  The  method  uses  the  gradients  of  the  loss 
function  with  respect  to  the  input  image  to  create  a  new  image  that 
maximises the loss. The new image is called the adversarial image. 
The  idea  is  to  maximise  loss  by  adjusting  the  input  data  directly  in  response  to 
back  propagated  gradients.  The  attack  adjusts  the  input  data  to  minimise  the 
loss. 
This can be summarised using the following expression :

![image](https://github.com/ssg1210/Measuring-the-effectiveness-of-FGSM-attacks-on-Deep-Neural-Networks/assets/167916988/4e35c9d4-5ce5-4096-b6cc-e7b3eecbadda)

where 
●  adv_x : Adversarial image. 
●  x : Original input image. 
●  y : Original input label. 
●  ϵ : Multiplier to ensure the perturbations are small. 
●  θ : Model parameters. 
●  J : Loss. 
There  is  an  interesting  property  of  the  gradient  vectors  that  are  taken  with 
respect  to  the  input  image.  This  is  done  in  order  to  create  an  image  that 
maximises  the  loss.  To  minimise  the  loss  value,  find  the  contribution  of  each 
pixel  to  the  total  loss,  and  adjust  the  perturbation  accordingly.  This  algorithm 
works  quickly  because  it  is  easy  to  find  the  required  gradients  using  the  chain 
rule.  Therefore,  the  gradient  is  obtained  for  the  image.  Since  the  model  is  no 
longer  being  trained,  the  model's  parameters  remain  constant.  The  goal  is  to 
deceive an already well-trained model.

It involves three steps in this order: 
1.  Calculate the loss after forward propagation, 
2.  Calculate the gradient with respect to the pixels of the image, 
3.  Nudge  the  pixels  of  the  image  ever  so  slightly  in  the  direction  of  the 
calculated gradients that maximise the loss calculated above. 
The  first  step,  calculating  the  loss  after  forward  propagation,  is  very  common 
in  machine  learning  projects.  We  use  a  negative  likelihood  loss  function  to 
estimate how close the prediction of our model is to the actual class.

# OUTPUT : FGSM ATTACK

![image](https://github.com/ssg1210/Measuring-the-effectiveness-of-FGSM-attacks-on-Deep-Neural-Networks/assets/167916988/77bb9027-e9c5-429f-976e-46462216eb84)

![image](https://github.com/ssg1210/Measuring-the-effectiveness-of-FGSM-attacks-on-Deep-Neural-Networks/assets/167916988/2243987c-530b-409d-929e-7ff2943dbf82)

![image](https://github.com/ssg1210/Measuring-the-effectiveness-of-FGSM-attacks-on-Deep-Neural-Networks/assets/167916988/b39b7a6e-8818-4197-9e56-e38a67f9d2fe)


