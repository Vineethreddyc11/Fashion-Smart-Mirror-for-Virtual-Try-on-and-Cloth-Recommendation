# Cloth Virtual Try-On and Recommendation

Developed hybrid approach for image based virtual try-on by reconstructing 3D cloth model of the target cloth by matching silhouettes to body model, transferring the 3D cloth model to the estimated 3D target human model, generating target human skin parts and blend it to the rendered warped cloth along with human representations.


![ed3c7757bda94ef69ecf0fe8f5b9e0fa](https://user-images.githubusercontent.com/68578215/199612732-2be33677-a573-4478-ac8d-28eb609a6f86.jpeg)

**The code will be posted after the paper is published in IEEE**

## Poster
 
<img width="770" alt="Screen Shot 2022-11-02 at 3 10 02 PM" src="https://user-images.githubusercontent.com/68578215/199612142-bcf120ee-d38e-437b-ab4d-5957e7bd17db.png">


## Project Architecture

<img width="723" alt="Screen Shot 2022-11-02 at 1 29 27 PM" src="https://user-images.githubusercontent.com/68578215/199596327-479f5808-2a87-4c16-a0b1-ddacf7756a3c.png">



## Project Background and Executive Summary
The fashion industry is an industry where customers belonging to all regions do sales by visiting the stores across the world. For every occasion or celebration, shopping for new clothes from fashion stores is quite common across the globe. Many people while shopping had to use the trial rooms to finalize the selection. However, in recent years with the advent of online shopping, people are buying clothes online. Online shopping has increased even further because of the pandemic, where people were not able to visit the stores in person. With the increase in sales of e-commerce sites across the world, researchers started focusing more on virtual try-on rooms which would enhance the e-commerce and fashion industries. According to the business research, the market for virtual fitting rooms can grow from $3.50 billion in 2021 to $12.97 billion in 2028 at a CAGR of 20.6% over the period 2021-to 2018. According to the global market forecast in Fashion AI, the market size of AI is expected to grow from $228 million in 2019 to $1260 million in 2028 at a CAGR of 40.8% for 2021-2018 .




<img width="694" alt="Screen Shot 2022-11-02 at 3 16 42 PM" src="https://user-images.githubusercontent.com/68578215/199613087-dfa4c822-0447-4acf-897d-48479c21cebd.png">


The idea of a virtual fitting room attracts almost every e-commerce user because of its simplicity, benefits, and ease of use. It is the concept where an end-user can try on the selected products like jewelry, shoes, glasses, or clothes using the cameras integrated with augmented reality and visualize how they look on the users. This helps both the customers and the retailers in the e-commerce industry to connect and benefit one another without any barriers like in-person visits of customers to the stores for shopping. The shopping experiences of customers in future times will seem to be completely different from the current ones because of the emerging technologies. There is a lot of research carried out in the field of virtual try-on in the past few years. The goal of many researchers is to create a seamlessly personalized system that helps customers with their shopping experience.  

One of the major aspects of our project is implementing virtual try-on using 3D modeling because of its growing demand and popularity. Virtual-try-on for apparel is a combination of computer vision, artificial intelligence, recommendation algorithms, and augmented reality (AR) or virtual reality (VR) [4]. There are lots of advancements in the technologies in the fields of virtual try-on, however, customers still wonder if the item that is selected would “fit” them correctly because different customers have a different point of view for the word “fit”. Secondly, modeling a human body in 3D would be difficult and few models are introduced recently. One more challenge while doing virtual shopping, the sizes vary according to the brand or region. It is hard to tell that everyone fits the standard mentioned sizes “S, M, L, X”.   

However, the advantages of using the Virtual try-on system are more when compared the disadvantages. One major advantage especially during the covid times is the contactless try-on that can happen using the virtual try-on approach. Many customers account for around 45% of total customers who agree that the use of AR helps to improve personalization and reduces the time and effort that they spent shopping. Many retailers are already using the Virtual try-on using the Kinect applications for letting the customers try on the glasses virtually [5]. There are also other AR applications like Fitnect and AM4U which are operated using Augmented Reality (AR) and help customers try-on things virtually [5]. One another advantage is it can reduce the returns related to Fashion. There is a good percent of online buyers who agree to buy the same version of one item across multiple sites to get a proper fit but with the use of virtual try-on one can easily see themselves if the selected item fits them perfectly or not. 

Another major part of our project is the Recommendation system. It is a system that recommends the end-user with a list of similar items based on his selection. This method helps to improve the shopping experiences of users by providing them with choices of similar items. The end-user has an option of changing the selection based on recommended items.  The recommendation of items happens concerning the features based on the user’s selection like color, gender, price, brand, etc. Therefore, the design of effective Recommendation systems helps the users gain good shopping experiences and the retailers increase their profits. Though a Recommendation system helps a lot in fashion e-commerce, not a lot of research has been done on Recommendation systems in the fashion industry.

The main idea of our project is to integrate both the systems of virtual try-on and Recommendations in combination with the smart mirror AR technology. We mainly focus on designing a seamless smart mirror-based Fashion AI, which helps the target user gain maximum shopping benefits. Our design is when the customer picks a product from the product catalog, we would recommend the customer with similar items which help the user have the best selection based on his preferences. Then after the selection of a particular item, we design the virtual try-on module which helps the user see how the selected product looks on him/her and have a good shopping experience by saving time and energy.

## Data Preprocessing

**Sample data before removing unnecessary data**

<img width="926" alt="Screen Shot 2022-11-04 at 8 09 05 AM" src="https://user-images.githubusercontent.com/68578215/200009687-003f7f9b-1b0c-4b46-add2-325a8c8823ec.png">
          

**Samples data after removing unnecessary data**


<img width="936" alt="Screen Shot 2022-11-04 at 8 09 35 AM" src="https://user-images.githubusercontent.com/68578215/200009684-2a8886c5-e350-4a66-912a-09111b0dbb65.png">

**Sample Complete Images**


<img width="961" alt="Screen Shot 2022-11-04 at 8 09 55 AM" src="https://user-images.githubusercontent.com/68578215/200009678-fa4a6506-05d3-4c3e-b69e-64998bc1adc9.png">

**Samples images after cropping**

<img width="940" alt="Screen Shot 2022-11-04 at 8 10 07 AM" src="https://user-images.githubusercontent.com/68578215/200009673-e0d81bb9-d7ec-4412-b057-8a606af07385.png">

**Sample images after adding a white background**

<img width="948" alt="Screen Shot 2022-11-04 at 8 10 13 AM" src="https://user-images.githubusercontent.com/68578215/200009668-02ba8e5c-85c8-4e9f-89eb-dc5fc0432555.png">

**Samples of images after resizing**

<img width="970" alt="Screen Shot 2022-11-04 at 8 10 24 AM" src="https://user-images.githubusercontent.com/68578215/200009665-5b4f78d4-7c3a-4e36-becb-c496ead442b6.png">

**Sample images before checking the orientation**
<img width="951" alt="Screen Shot 2022-11-04 at 8 10 34 AM" src="https://user-images.githubusercontent.com/68578215/200009663-1dbe0215-c450-493f-b049-32b8a0372de6.png">

**Sample images after orientation**

<img width="948" alt="Screen Shot 2022-11-04 at 8 10 41 AM" src="https://user-images.githubusercontent.com/68578215/200009660-22ab712d-6956-4e97-ac40-a26d11f350d6.png">

**Sample images for the recommendation for male in the training dataset**


<img width="959" alt="Screen Shot 2022-11-04 at 8 10 52 AM" src="https://user-images.githubusercontent.com/68578215/200009655-2e44e497-53e5-4237-8545-d50ed2ef5b78.png">

**Sample images for a recommendation for female in the training dataset**

<img width="968" alt="Screen Shot 2022-11-04 at 8 10 58 AM" src="https://user-images.githubusercontent.com/68578215/200009643-99b70838-ade8-4f9d-a00c-07f769cec685.png">

**Sample images for virtual try-on for males in the training dataset**


<img width="955" alt="Screen Shot 2022-11-04 at 8 11 32 AM" src="https://user-images.githubusercontent.com/68578215/200009637-3960620f-e722-45e7-8cb9-ad7c672af053.png">

**Sample images for virtual try-on for females in the training dataset**

<img width="957" alt="Screen Shot 2022-11-04 at 8 11 37 AM" src="https://user-images.githubusercontent.com/68578215/200009618-020df444-8ba2-4769-b009-ff6d5112b175.png">


## Model 
**Segmentation Generation Network:** The Semantic Segmentation Network is used to generate the target human body model mask according to the target cloth shape. The segmentation generation network (SGN) takes the target user image as input and then generates the mask which is in the shape of the target cloth. This model is implemented using the GAN model where the generator is the U-Net model, and the discriminator is the Pix2PixHD. The separate mask generation for the target user as per the target in-shop image is implemented first time in the CloTH-VTON model when compared to other models like VITON, and CP-VTON  which are the different VTON models.

**3D Cloth model using Reconstruction of In-shop image:** To carry out this task, we have various sub-tasks which include Mask Generation Network, 2D cloth matching, 3D models Reconstruction, parameter estimation, and Model Deformation. 

**Mask-Generation Network:** The Mask generation Network is used to generate the cloth mask for 2D cloth matching. In earlier works, the 3D garment Reconstruction is done manually using a limited number of product categories. In earlier works, they mainly train separate models using garment templates for predicting the 3D body model. But the proposed model which is like the model proposed by Minar et al. uses the 3D human body model which is the SMPL body model to match the 2D silhouette 

**2D cloth matching:**  Initially, shape context matching (SCM) is applied between target clothes and the corresponding categorical masks. Next,  thin-plate spline transformation (TPS) is applied to the target cloth to match the shape correspondences of SCM. Finally, the clothing textures are aligned to the SMPL body model. 

**3D Model Reconstruction:** In this step, the 3D model is constructed as per the shape of the target user. To do that, initially, the 3D human body model is projected into a 2D image space. Once the vertices are in 2D space, these are mapped to the vertices of the cloth image. Then to do a smooth process of the clothes and shape transformation, the cloth vertices are mapped to the 3D human model. The corresponding points in the clothing boundary are defined as the closest points to the projected vertices. We estimate Thin-Plate Spline (TPS) [63] parameters and apply them to the mesh points. New mesh points are considered as the vertices projected from the 3D mesh of clothing Clothed. From 2D points to 3D points are done with inverse projection with depth obtained from the body with a small constant gap. 

**Human Model Parameter Estimation:** The human model parameters are estimated using the SMPLify method. A better can be still used when compared to SMPLify as it is only for full-body images. 


**Try-on Fusion:** The try-on function module is where we get the final output of the VITON system. In this, it mainly has the parts Generation Network (PGN) [7] and then fusion of everything. 

**Parts-Generation Network:** The Parts generation network is mainly used to generate the target-user parts like the face, neck, and torso as per the user's skin color. The PGN takes the target-user segmentation output and the target user's skin color as input and then generates the upper body parts of the target user. The PGN architecture is also like the architecture of SGN and MGN used earlier. It uses GAN where U-Net acts as a generator and Pix2PixHD [7] acts as the discriminator. 

- Finally, all the parts are merged which include a 3D human model, parts generated, and 3D warped cloth. All together forms the output of the VITON system. 



**Model Deformation:** Till now, 3D clothing models and 3D reconstructions for standard shaped and posed person. To achieve the output of the VTON system, we need to transfer the shape and pose coordination of the target user to the obtained 3D model. Instead of directly applying the pose and shape parameters to the 3D model, we use displacements of vertices as it gives us more natural results. Now as we have the deformed model, we need to attach the warped in-shop cloth image to this model. 

## Model Architecture
<img width="724" alt="Screen Shot 2022-11-02 at 1 29 05 PM" src="https://user-images.githubusercontent.com/68578215/199596337-17c32178-d202-4a3e-b9e0-86eb4a3d6579.png">


