# Welcome to E-Flower 
- About: An application that detect flowers given an close-up image of that flower
- Author: Nhu Nguyen, Christy Nguyen, Diem Vu, Hong Vu
- Advisor: Haonan Wang
- Organization: San Jose State University
- Course: CMPE195A/B - Senior Project
- Main reference: https://arxiv.org/pdf/2106.04803v2.pdf
# About The Model
E-Flower integrates CoAtNet, a product of combining convolution neural networks (CNN) and attention-based transformation logics. 
## CNN
CNN is dominating in the computer vision field for it's inductive bias, meaning this algorimth is ideal for making prediction with less training images.
## Transformer 
On the other hand, self-attention models such as Vision Transformer (ViT) is used for natural language processing, hence used in written/spoken language intepretation, a virtual assistance for example.  
## CoAtNet
To take advantage of both these models, CoAtNet (**Co**nvolutional and self-**At**tention **Net**work) implement the stacking of CNN and transformer layers.
Different combinations of C and T blocks were experiences with, and C-C-T-T gives the best results. 
# Our Application
## Database
Our complete database consist of nearly 100 flower categories, with each categories containing over 400 images.
## Data Processing
To put CoAtNet to a practical use, our team implemented a data-processing layer to feed in flower images.
*With the purpose of reaching high accuracy while staying in the low-data regime, we limited the number of flower categories to only 5. The prototype dataset includes roses, sunflowers, daisys, dandelions, and tulips. Furthermore, we increase the number of images in each categories to over 1k.* 
## Testing
After training CoAtNet with the prototype dataset, which reached the highest accuracy of 85%, we implement a simple testing to assess the model's accuracy one more time, as well as . 
## Web Application
Our application is saved and exported to Anvil to provide a simple GUI for a more user friendly interface.

# Usage Instruction
## For developers to reproduce E-Flower
1. Make a copy of the **flower_category.ipynb** Google Colab notebook
2. Connect to a runtime on Google Colab
3. Compose a database of your choice, sort same flowers into folder with the flower's name as the folder's name
4. Upload the database to Google Drive
5. Replace the paths in the **split_data** cell with your paths 
6. Go over each cell and run

## For user to use the webapp
1. Navigate to https://yv6zqaazvbpttrub.anvil.app/R766MVIZQBKRA65653RMGC2P
2. Download an image of a flower (for now, E-Flower only recognizes roses, sunflowers, daisys, dandelions, and tulips)
3. Press the **Upload** button
4. Press the **Submit** button
5. Repeat steps 2-4 if desired
