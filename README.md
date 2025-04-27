# machine-learning-homework-11-solved
**TO GET THIS SOLUTION VISIT:** [Machine Learning Homework 11 Solved](https://www.ankitcodinghub.com/product/machine-learning-solved-12/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;121248&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Machine Learning Homework 11 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
Machine Learning HW11

Outline Links

● Task Description ● Kaggle

● colab tutorial

● Dataset ● HW11 dicussion

● Data &amp; Submission Format

● Grading Policy

Task Description – Domain Adaptation

● Imagine you want to do tasks related to the 3D environment, and then discover that…

○ 3D images are difficult to mark and therefore expensive.

○ Simulated images (such as simulated scene on GTA-5) are easy to label.

Why not just train on simulated images?

Task Description – Domain Adaptation

Net (D)

Net (U)

Feat A

Output

????

????

● For Net, the input is “abnormal”, which makes Net doesn’t work properly.

???

Task Description – Domain Adaptation

Net (D)

Net (U)

Output

Output

● Therefore, one simple way to solve this problem is to make the distributions of FeatA and FeatB similar.

similar

Task Description – Domain Adaptation

● Our task: Given real images (with labels) and drawing images (without labels), please use domain adaptation technique to make your network predict the drawing images correctly.

Dataset

● Label: 10 classes (numbered from 0 to 9), as following pictures described.

● Training : 5000 (32, 32) RGB real images (with label). ● Testing : 100000 (28, 28) gray scale drawing images.

Data Format

● Unzip real_or_drawing.zip, the data format is as below: ● real_or_drawing/

○ train_data/

■ 0/

● 0.bmp, 1.bmp … 499.bmp

■ 1/

● 500.bmp, 501.bmp … 999.bmp

■ … 9/

○ test_data/

■ 0/

● 00000.bmp

● 00001.bmp

● … 99999.bmp

Data Format

● You can simply use the following code to get dataloader after extracting the zip. (You can apply your own source/target transform function.)

source_dataset = ImageFolder(‘real_or_drawing/train_data’, transform=source_transform) target_dataset = ImageFolder(‘real_or_drawing/test_data’, transform=target_transform)

source_dataloader = DataLoader(source_dataset, batch_size=32, shuffle=True) target_dataloader = DataLoader(target_dataset, batch_size=32, shuffle=True) test_dataloader = DataLoader(target_dataset, batch_size=128, shuffle=False)

Submission Format

● First line should be “id, label”.

● Next 100, 000 lines are your predicted labels of test images.

● Evaluate Metrics = Accuracy.

Grades

● +0.5pt : Simple public baseline (0.44616) ● +0.5pt : Simple private baseline

● +0.5 : Medium public baseline (0.64576) ● +0.5 : Medium private baseline

● +0.5 : Strong public baseline (0.75840) ● +0.5 : Strong private baseline

● +0.5 : Boss public baseline (0.80640)

● +0.5 : Boss private baseline

● +4pt : report submisssion / +2pt : code submission

Baseline Guides

● Simple Basline (0.5 + 0.5 pts, acc≥0.44616, &lt; 1hour) ○ Just run the code and submit answer.

● Medium Baseline (0.5 + 0.5 pts, acc≥0.64576, 2~4 hours) ○ Set proper λ in DaNN algorithm. ○ Luck, Training more epochs.

● Strong Baseline (0.5 +0.5 pts, acc≥0.75840, 5~6 hours)

○ The Test data is label-balanced, can you make use of this additional information?

○ Luck, Trail &amp; Error 🙂

*影片中的 baseline 和投影片有些微差異，請以投影片和 kaggle 的分數為主

Baseline Guides

● Boss Baseline (0.5 + 0.5 pts, acc ≥0.80640)

○ All the techniques you’ve learned in CNN.

■ Change optimizer, learning rate, set lr_scheduler, etc… ■ Ensemble the model or output you tried.

○ Implement other advanced adversarial training. ■ For example, MCD MSDA DIRT-T

○ What about unsupervised learning? (like Universal Domain Adaptation?)

*影片中的 baseline 和投影片有些微差異，請以投影片和 kaggle 的分數為主

Grading — Bonus

● If your ranking in private set is top 3, you can choose to share a report to NTU COOL and get extra 0.5 pts.

● About the report

○ Your name and student_ID ○ Methods you used in code

○ Reference Report Template

○ in 200 words

○ Please upload to NTU COOL’s discussion of HW11

Code Submission – NTU COOL

● NTU COOL

○ Compress your code and report into &lt;student_ID&gt;_hw11.zip（e.g. b10123456_hw11.zip） ○ We can only see your last submission.

○ DO NOT submit your model or dataset.

○ If your code is not reasonable, your semester grade x 0.9.

● Your .zip file should include only

○ Code: either .py or .ipynb

Question1(+2 pts): Visualize distribution of features accross different classes.

1. Please make t-SNE plot the distribution of early, middle, final stage.

a. Evaluate the model on training dataset, collect features and labels

b. Make 3 t-SNE plots of the following training phase:

i. early stage

ii. middle stage

iii. final stage

2. Explain and analyze the distribution of feactures of three stages.

a. Hint: Is is a good feature extractor for classification task? Why or Why not?

t-SNE 課程連結

3. Example plot &amp; Hints

– SKlearn provide t-SNE function: link

– Normalize the output before plotting

– cmap is convenient to map colors

Final Stage

Quesion2 (+2pts): Visualize distribution of features accross different domains.

1. Please plot the distribution of early, middle, final stage.

a. Evaluate the model on source dataset and target dataset, collect feature and labels

b. Make 3 plots of the following training phase:

i. early stage

ii. middle stage

iii. final stage

2. Explain and analyze the distribution of feactures of three training phases.

a. Hint: Is is a good feature extractor for domain adaption task? Why or Why not?

t-SNE 課程連結

3. Example plot &amp; Hints

– The label is related to the domain

e.g. “1” for source and “0” for target

– Target dataset is too large. Just randomly pick 5000 images to evaluate.

Final Stage

● Question1 (+2pts)

– Include 3 t-SNE plots of different phase accross different classes.

– Compare the plots and give simple explanation on the distribution of the features.

● Question2 (+2pts)

– Include 3 t-SNE plots of different phase accross source and target domains.

– Compare the plots and give simple explanation on the distribution of the features.

Regulations

● You should finish your homework on your own.

● You should not modify your prediction files manually

● Do not share codes or prediction files with any living creatures.

● Do not use any approaches to submit your results more than 5 times a day.

● Do not search or use additional data or pre-trained models.

● Your final grade x 0.9 and this HW will get 0 pt if you violate any of the above rules.

● Prof. Lee &amp; TAs preserve the rights to change the rules &amp; grades.

Contact us if you have problems…

● NTU COOL (Best way) ○ link

● Email

○ The title should begin with “[hw11]”

Learning Curve (Loss)

● This image is for reference only.

Iterations

Learning Curve (Accuracy)

● This image is for reference only.

● Note that you cannot access testing accuracy.

● However, this plot tells you that even though the model overfits the training data, the testing accuracy is still improving.

● Basic version of DaNN (Domain-Adversarial Training of NNs)

● The training will lose control if the model have input with different ditribution from training dataset, as shown below.

● Why can’t the CNN model predict correctly when evaluating on dataset B?

A: Becase there is no label for dataset B.

A dataset (∈ Training)Normal Output

B dataset (∉ Training)Abnormal Output

● To resolve this issue, DaNN seperate the CNN into 2 parts.

● The goal is to make the output of feature extractor has simliar distribution when evealuating on dataset A and dataset B.

A dataset (∈ Training)Normal Normal

Output

Output

B dataset (∉ Training)Try to Normal

become Output

Normal

Output

● How to make the model has similiar distribution in spite of evaluating on dataset with different distributions ?

● A: The simplest solution is to apply a discriminator in GAN to predict the domain. So the feature extractor need to deceive the domain classifier. As a result, the feature output will have similiar distribution.

Become

B’s normal

A dataset (∈ Training)Output Discriminator / is A dataset

Domain

B dataset (∉ Training)BecomeA’s Normal Classifier is B dataset

Output,

deceive discriminator
