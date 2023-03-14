# HW6

kNN

In this part, we’ll implement our first machine learning algorithm of the course – k Nearest Neighbors. We are considering a binary classification problem where the goal is to classify whether a person has an annual income more or less than $50,000 given census information. As no validation split is provided, you’ll need to perform cross-validation to fit good hyperparameters.

We’ve done the data processing for you for this assignment; however, getting familiar with the data before applying any algorithm is a very important part of applying machine learning in practice. Quirks of the dataset could significantly impact your model’s performance or how you interpret the outcome of your experiments. For instance, if I have an algorithm that achieved 70% accuracy on this task – how good or bad is that? We’ll see! We’ve split the data into two subsets – a training set with 7,000 labelled rows, and a test set with 1,000 unlabelled rows. These are “train.csv” and “test_pub.csv”.

Both files will come with a header row, so you can see which column belongs to which feature. Below you will find a table listing the attributes available in the dataset. We note that categorizing some of these attributes into two or a few categories is reductive (e.g. only 14 occupations) or might reinforce a particular set of social norms (e.g. categorizing sex or race in particular ways). For this homework, we reproduced this dataset from its source without modifying these attributes; however, it is useful to consider these issues as machine learning practitioners.

- **attribute name:** *type.* list of values
- **id:** *numerical.* Unique for each point. Don’t use this as a feature (it will hurt, badly).
- **age:** * numerical.
- **workclass:** *categorical.* Private, Self-emp-not-inc, Self-emp-inc, Federal-gov, Local-gov, State-gov, Without-pay
- **education-num:** *ordinal.* 1:Preschool, 2:1st-4th, 3:5th-6th, 4:7th-8th, 5:9th, 6:10th, 7:11th, 8:12th, 9:HS-grad, 10:Some-college, 11:Assoc-voc, 12:Assoc-acdm, 13:Bachelors, 14:Masters, 15:Prof-school, 16:Doctorate
- **marital-status:** *categorical.* Married-civ-spouse, Divorced, Never-married, Separated, Widowed, Married-spouse-absent, Married-AF-spouse
- **occupation:** *categorical.* Tech-support, Craft-repair, Other-service, Sales, Exec-managerial, Prof-specialty, Handlerscleaners, Machine-op-inspct, Adm-clerical, Farming-fishing, Transport-moving, Priv-house-serv, Protective-serv, ArmedForces
- **relationship:** *categorical.* Wife, Own-child, Husband, Not-in-family, Other-relative, Unmarried
- **race:** *categorical. White, Asian-Pac-Islander, Amer-Indian-Eskimo, Other, Black
- **sex:** *categorical. 0:Male, 1:Female
- **capital-gain:** *numerical.*
- **capital-loss:** *numerical.*
- **hours-per-week:** *numerical.*
- **native-country:** *categorical.* United-States, Cambodia, England, Puerto-Rico, Canada, Germany, Outlying-US(GuamUSVI-etc), India, Japan, Greece, South, China, Cuba, Iran, Honduras, Philippines, Italy, Poland, Jamaica, Vietnam, Mexico,
Portugal, Ireland, France, Dominican-Republic, Laos, Ecuador, Taiwan, Haiti, Columbia, Hungary, Guatemala, Nicaragua,
Scotland, Thailand, Yugoslavia, El-Salvador, Trinada&Tobago, Peru, Hong, Holand-Netherlands
- **income:** *ordinal.* 0: <=50K, 1: >50K This is the class label. Don’t use this as a feature.
O
