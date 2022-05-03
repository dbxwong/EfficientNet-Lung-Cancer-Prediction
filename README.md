## CHEST CT SCAN LUNG CANCER PREDICTION

## IMPETUS 
Worldwide, an estimated 19.3 million new cancer cases (18.1 million excluding nonmelanoma skin cancer) and almost 10.0 million cancer deaths (9.9 million excluding nonmelanoma skin cancer) occurred in 2020. Female breast cancer has surpassed lung cancer as the most commonly diagnosed cancer, with an estimated 2.3 million new cases (11.7%), followed by lung (11.4%), colorectal (10.0 %), prostate (7.3%), and stomach (5.6%) cancers. Lung cancer remained the leading cause of cancer death, with an estimated 1.8 million deaths (18%), followed by colorectal (9.4%), liver (8.3%), stomach (7.7%), and female breast (6.9%) cancers [Source](https://acsjournals.onlinelibrary.wiley.com/doi/10.3322/caac.21660). On a personal note, I picked lung cancer prediction having lost a grandmother to the disease.

Access to medical facilities afflict many under developed/developing communities. The ongoing COVID-19 health crisis further taxes over-burdened healthcare systems. Despite the heavy resources being focussed on COVID-19 managmenet, lung cancer continues to afflict many worldwide and may not be picked up till Stage 3 or 4, when it is often too late for intervention. This motivates the creation of a efficient means to diagnose lung cancers to enable commencement of early intervention.

EfficientNet-B4 was selected as a more compact choice over prior work done with the the largest B7 model. Compared with the widely used ResNet-50, EfficientNet-B4 uses similar FLOPS, while improving the top-1 accuracy from 76.3% of ResNet-50 to 82.6% (+6.3%), based on this [source](https://ai.googleblog.com/2019/05/efficientnet-improving-accuracy-and.html).

## DATA

Access to medical data is tough especially for those not in the field. To this end, we use [Kaggle's Chest CT-scan dataset](https://www.kaggle.com/datasets/mohamedhanyyy/chest-ctscan-images) to build and validate our model on the assumption the carcinoma presented in the dataset generalizes well to carcinoma in humans elsewhere else. 

The dataset contains 3 cancer lung cancer types: Adenocarcinoma, Large cell carcinoma, Squamous cell carcinoma, normal, non-cancerous cells.

Adenocarcinoma Adenocarcinoma of the lung: Lung adenocarcinoma is the most common form of lung cancer accounting for 30 percent of all cases overall and about 40 percent of all non-small cell lung cancer occurrences. Adenocarcinomas are found in several common cancers, including breast, prostate and colorectal.

Adenocarcinomas of the lung are found in the outer region of the lung in glands that secrete mucus and help us breathe. Symptoms include coughing, hoarseness, weight loss and weakness.

Large cell carcinoma Large-cell undifferentiated carcinoma: Large-cell undifferentiated carcinoma lung cancer grows and spreads quickly and can be found anywhere in the lung. This type of lung cancer usually accounts for 10 to 15 percent of all cases of NSCLC. Large-cell undifferentiated carcinoma tends to grow and spread quickly.

Squamous cell carcinoma Squamous cell: This type of lung cancer is found centrally in the lung, where the larger bronchi join the trachea to the lung, or in one of the main airway branches. Squamous cell lung cancer is responsible for about 30 percent of all non-small cell lung cancers, and is generally linked to smoking.

## RESULTS

Using EfficientNet B4, results were obtained after 8 Epochs with a comparison of training and validation model metrics shown here:

![EfficientNet LungCancerNet](https://user-images.githubusercontent.com/40510434/166460944-df78e6b7-2327-4b8e-a5a6-b2f2d0bdfcaf.PNG)

<img width="1000" alt="EfficientNet LungCancer" src="https://user-images.githubusercontent.com/40510434/166460333-a12ac703-6e2b-453c-821f-27352b9574e4.PNG">

## FUTURE WORK

To improve the performance of the luncg cancer predictor,  I'd recommend retraining with additional clinical data to incorporate cancer cell presentation across various age groups. Lung cancer is a far more complex disease beyond the classes presented in this project.


--------------------------------------------------------------------------
MIT License

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
