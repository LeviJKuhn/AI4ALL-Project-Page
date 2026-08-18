# Solar Panel Defect Detection Model  
Created a ResNet-18 computer vision model to classify solar panel defects. Utilizing transferred learning techniques to increase model efficacy, stratified sampling methods to ensure equal representation, and GradCAM to create model explainability for informed decision making, all within AI4ALL's cutting-edge AI4ALL Ignite accelerator.  


## Problem Statement <!--- do not change this line -->  
As carbon emissions continue to climb, scientists and engineers are looking for ways to implement and improve upon existing clean energy solutions. Current clean energy solutions come with large, up-front costs or long-term maintenance plans. By reducing the necessary human labor, and resulting monetary cost, of maintaining these clean energy solutions, they can more easily be adopted internationally.  

## Key Results <!--- do not change this line -->
1. Fine-tuned a ResNet18 classifier to 88.14% test accuracy across six solar panel
   conditions (Bird-drop, Clean, Dusty, Electrical-damage, Physical-Damage, Snow-Covered),
   evaluated on a held-out stratified test set of 177 images.

2. Compared stratified against simple random sampling for the train/test split.
   Stratified sampling scored 88.14% versus 84.75% for a random split, but this 3.4-point
   gap represents only 6 images out of 177 and falls within run-to-run noise, so it should
   not be read as evidence that stratification improves accuracy. Stratification was
   retained because it guarantees the test set reflects the true class distribution, making
   per-class metrics interpretable and comparable across runs.

3. Identified per-class performance as uneven, with accuracy varying substantially
   across conditions:
   - Snow-Covered: 100% (25/25)
   - Clean: 94.74% (36/38)
   - Bird-drop: 87.80% (36/41)
   - Electrical-damage: 85.71% (18/21)
   - Dusty: 84.21% (32/38)
   - Physical-Damage: 64.29% (9/14) — the weakest class, and also the smallest, with only
     14 test images; the small sample makes this estimate imprecise.

5. Applied GradCAM to visualize model attention, confirming the classifier focuses on the panel surface rather than background artifacts.

6. Deployed an interactive Streamlit application that accepts an uploaded panel image
   and returns a predicted condition with per-class confidence scores.


## Methodologies <!--- do not change this line -->

(UPDATE IN README.md)

*EXAMPLE:*
*To accomplish this, we utilized the OpenAI API to interact with ChatGPT, and we designed a custom Python script to generate diverse prompts and collect corresponding responses. The data was then processed and analyzed using pandas, enabling us to detect patterns and biases in the AI model's outputs.*
*Engineered a Python script to generate over 1,000 prompts and elicit their responses from ChatGPT, utilizing pandas to collect the data. When prompted for solutions to this specific relevant crisis, nearly 80% of ChatGPT's responses promoted a certain worldview.*


## Data Sources <!--- do not change this line -->

(UPDATE IN README.md)
Include any relevant data sources that were used in your project.

*EXAMPLE:*
*Kaggle Datasets: [Link to Kaggle Dataset](https://www.kaggle.com/datasets)*

## Technologies Used <!--- do not change this line -->

(UPDATE IN README.md)
List the technologies, libraries, and frameworks used in your project.

*EXAMPLE:*
- *Python*
- *pandas*
- *OpenAI API*


## Authors <!--- do not change this line -->

(UPDATE IN README.md)
List the names and contact information (e.g., email, GitHub profiles) of the authors or contributors.

*EXAMPLE:*
*This project was completed in collaboration with:*
- *John Doe ([john.doe@example.com](mailto:john.doe@example.com))*
- *Jane Smith ([jane.smith@example.com](mailto:jane.smith@example.com))*
