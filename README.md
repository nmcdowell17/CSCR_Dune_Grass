# CSCR_Dune_Grass 
--> this directory and the work the CSCR Dune Grass Project has done seeks to build a methoid for predicting the precent coverage of Dune Grass qudrat sites based on % coverage Data  

# Defintions 
1) Qudrat Site = induvidal feild site ( used as image feutre data) of Dune grass. These images were taken overhead by drone or by cellphone camera
2) % Coverage = metric for tracking how much of qudrat site was covered and instead of just a float value was broken into five categories (0%,1-25%,26-50%,51-75%,76-100%)

# Dask pipeline 
--> A dask pipeline had to be added on to execute the preprocessing work in parallel, since we ran into problems running it on smaller pc units. The VN we were running it on at the moment was --- in size 

# Preprocesing 
--> The preprocesing has three main compents: 
1) Grounding Dino  to take text input + qudrat site =  mediocore bounding box)
2)  Segment Anything model which takes medocoire bounding box + image = realy accurate mask of inside of qudrat
3)   Corner detection based on mask for realy accurate bounding box
4)   crop and undisort images --> get inside of the cite

# CNN Architecture 
--> The model uses transfer learning from Resnet + attaches head to it to filter for the four categories 
--> An image generation scheme was also used inorder to provided the model with more data

