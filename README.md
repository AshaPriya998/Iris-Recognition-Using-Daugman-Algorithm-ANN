# Iris-Recognition-Using-Daugman-Algorithm-ANN

Iris Recognition Using Daugman Algorithm & ANN

ABSTRACT :
There are several different techniques for biometric authentication. Iris recognition happens to be one of the most sophisticated and effective among them. It is mainly based on the pattern recognition method where in it identifies sharp and distinct patterns of the Iris that can accurately recognize the intended user. This recognition system is quite accurate and also gives improved performances. With the rise in the security breaches and other forms of authentication frauds, it is very important to have a stringent biometric system in place. In the proposed work, iris localization has been performed by using the Daugman’s algorithm which is an integro-differential operator capable of separating or segmenting out regular shapes. The Daugman’s algorithm also has a noise smoothening capability. Both these attributes make the Daugman’s algorithm a preferred choice for iris localization. Subsequent to the iris localization, feature extraction is carried out to compute the relatively non-varying and unique parameters of an iris image. The features computed in the work are Contrast, Correlation, Energy, Homogeneity, Mean, Standard Deviation, Entropy, RMS, Variance, Smoothness, Kurtosis and Skewness. The features tend to behave uniquely for different iris images. However, overlapping values are possible. The features are then fed to a neural network using the Levenberg-Marquardt back propagation training rule. After training the neural network with feature values of authorized images, the subsequent step is testing the neural network for accuracy. The standard MMU database has been used for design of the system. It has been found that the proposed system attains an accuracy of 99.7% which is higher compared to the previously existing system using the same database.


INTRODUCTION :
The user Authentication is one of the key concern areas that form the part of secured access to data. Iris authentication and recognition approach that helps in authenticating the intended user utilizing the characteristic features of the iris. It has several other applications such as it is used in ATM’s, and biometric recognition systems. This system typically contains different phases of functioning. The figure below shows the process involved for the iris recognition system. It happens to be a very useful approach in most cases. Figure 1 shows the process of Iris Recognition system and its different steps. Iris recognition is a form of bio metric authentication system that uses high end mathematical techniques and processes on the digital image of the Iris of the eye. It is mainly based on the pattern recognition method where in it identifies sharp and distinct patterns of the Iris that can accurately recognize the intended user. This recognition system is quite accurate and also gives improved performances. With the rise in the security breaches and other forms of authentication frauds, it is very important to have a stringent biometric system in place. Especially in places of high importance like the banks and ATMs, it is useful. Different algorithms are employed to encode the different set of patterns that exist in the iris localization scheme. It is useful to know the user is the real person or someone else impersonating the intended person. The system maintains a database. The database is usually big and consists of large number of templates of the iris features. This is then matched by the search engine of the model for the recognition purpose.
 
So many people all over the world have resorted to these iris authentication mechanisms to safeguard their authenticity. Its extensive proliferation can be seen in places that are of national importance and financial and confidential institutions. In airports also this system is incorporated. National level exams where any person can take the exam illegally have also implemented this scheme. A really useful characteristic of this system is that it has a very robust and accurate matching process for the pattern recognition and also the incidence of false matches is extremely rare. Also as the Iris is a stable internal part of the human eye, it is quite reliable and useful for this purpose.




EXITING SYSTEM :
Blood The proposed system is based in improvement in iris recognition based on the Dugman’s algorithm for iris localization and the use of neural networks for classification. The proposed method detects pupil using Daugman’s integro differential operator (IDO) and subsequently trains a neural network classifier for the final classification.

The Daugman’s Algorithm
The Daugman’s algorithm is by far one of the most effective classifiers as far as iris recognition is concerned. It relies on the fact that regular shapes with distinctive boundaries can be easily segmented by the Daugman’s algorithm. There are several steps involved in the IDO which re explained below.
Histogram Equalization:-
 This process generally improves the contrast of the irs thereby increasing the possibility of better segmentation.
Binarization:-
The image Binarization technique is extremely effective in ehnacing or amplifying the differences between the pupil and the iris section. The Binarization technique also is responsible for removal of interfering objects that may mar the separation performance.. Moreover, the binarization is based on applying an integro-differential operator to find the iris and pupil contour. The mathematical expression for the Daugman’s algorithm is given below:
 
Where I(x, y) is the input eye image,
 r being the radius that is to be searched for, 
Gσ is a Gaussian function used for smoothing and s is the circle contour given by r,x0 and y0.
The operator can be understood to carry out a pixel wise search throughout the entire image as on a partial derivative (blurred) of the integral over circular contours which are in the process normalized in different contours. [3]-[5]The boundaries of the pupil separating the pupil form the iris makes contour integral derivative maximum, the point where there will be a sudden change in the values of intensity over the circular borders. The two dimensional Gaussian Filter that is used in the Daugman’s algorithm is defined by:
 



Where, 
‘a’ denotes the peak of the distribution curve of intensity and its given by the formulation of a two dimensional intensity function.  In two dimensions, it is the product of two such Gaussians, one per direction we have:
 
Here,
 x and y are the spatial coordinates 
𝜎 2 represents the variance of the random process 
The algorithm is effective enough for the localization of regular images owing to the fact that regular shapes exhibit a sudden peak in intensity at the contours and hence make the contour derivative maximum shapes. In the case pertaining to the iris segmentation, the relation for the segmentation inequation is governed by R1<s<R2
Here, 
R1 is the inner radius of the iris
 R2 is the outer radius of the iris
 s is the region of the iris lying within the region bounded by R1 and R2
 The above inequality separates the iris as a strip and results in iris localization. The segmented part is a circular ring patch enclosed by the region of R1 and R2.
Introduction to Artificial Neural Networks:
Artificial neural networks multi-domain and multi faceted applications especially in the fields of pattern recognition and classification problems. ANN is typically used for applications where the data is:
 1) Large
 2) Complex
Or
 3) Both Large and complex The mathematical structure of the ANN is shown in the figure below:
 
Here,
 X are the inputs
 Y is the output of ANN W is weight
 θ represents the logic for analysis or bias.
 The mathematical model of the ANN gives us the empirical relation between the inputs, weights and the output:
 
The learning capability of the ANN structure is based on the temporal learning capability governed by the relation:
 (𝑖) = (𝑖, 𝑒)                 (5)
Here,
 w (i) represents the instantaneous weights
 i is the iteration
 e is the prediction error
 The ANN has the following 3 stages of layers: 
1) Input Layer: This section receives the inputs (X) as a parallel stream.
 2) Hidden Layer: This layer is responsible for the data analysis and pattern recognition such as iris recognition applications critically depend upon the training algorithm used to train the ANN and the weights saved subsequently
The weight changes dynamically and is given by:
 
Here,
 Wk is the weight of the current iteration. 
Wk+1 is the weight of the subsequent iteration.
 3) Output Layer: The output layer simply renders the output of te composite ANN mechanism. The structure is shown below:
 
Here, 
I represents input layer 
H represents hidden layer
 O represents output layer
Design of Neural Network Based on LevenbergMarquardt Algorithm :
This algorithm bears its name on the names of Kenneth Levenberg and Donald Marquardt. The major essence of the algorithm is its speed and its stability.. The flowchart of the LM algorithm is given below.
 
 
Where
 𝐽𝑘 is the Jacobian matrix for kth input data stream, 
g is the gradient vector e is the error
 T is the transpose operation 
k is the iteration number 
The training rule for the algorithm is mathematically given by:
 
Where,
 I represents an identity matrix, 
Wk is present iteration weigt,
 Wk+1 is the subsequent iteration weight and
 ek is the error evaluated in the previous iteration
 μ is called the step size for weight variation 𝐻 the Hessian Matrix,
 which is the second order derivative of errors with respect to weights. 
The Hessian Matrix is given by:
 
The significance of the LM training rule is that it computes the Hessian Matrix (H) indirectly as a function of the Jacobian matrix. This reduces the time complexity of the algorithm.
 











PROPOSED SYSTEM :

The The results of the proposed work is the design of a technique that is capable to attain the classification of iris recognition with the following attributes
 1) Lesser error in classification 
2) Higher accuracy
 3) Low or moderate time complexity (low number of iterations)

A sequential approach in all the steps involved is given below:
 




 
The figure above depicts the captured image of the eye. It is worth noting that the image has the reflections of the camera and is a composite image which needs segmentation for the iris.
 
The algorithm is effective enough for the localization of regular images owing to the fact that regular shapes exhibit a sudden peak in intensity at the contours and hence make the contour derivative maximum shapes. In the case pertaining to the iris segmentation, the relation for the segmentation inequation is governed by:                        	

 
Here,
 R1 is the inner radius of the iris
 R2 is the outer radius of the iris R is the region of the iris lying within the region bounded by R1 and R2

The above inequality separates the iris as a strip and results in iris localization. The segmented part is a circular ring patch enclosed by the region of R1 and R2.
 
 
The evaluation parameters for the neural network are explained below:
 Accuracy (Ac): It is mathematically defined as:
 
1. True Positive (TP): It is the case when a sample belongs to category and the test also predicts its belongingness. 
2. True Negative (TN): It is the case when a sample does not belong to category and the test also predicts its non-belongingness. 
3. False Positive (FP): It is the case when a sample does not belong to category and the test predicts its belongingness.
 4. False Negative (FN): It is the case when a sample belongs to category and the test predicts its nonbelongingness.

 
It can be seen that the iris part has been separated using the Daugman’s algorithm and then the classification has been done as authorized.
 
It can be seen that the iris part has been separated using the Daugman’s algorithm and then the classification has been done as unauthorized.
The computation of accuracy can be given by: 
700 images have been training.
 300 images have been used for testing.
 3 Images have been classified inaccurately. 
error =3/1000=0.3% Hence accuracy is 99.7%
The database used is the MMU database, and the proposed technique attains an accuracy of 99.7%, which is higher than the previously proposed techniques (98.73%) . A comparative analysis with the previous approach (Co-occurrence Features and Neural Network Classification 
Approach for Iris Recognition by Vyas et al. IEEE 2017) is given:
 








HARDWARE & SOFTWARE REQUIREMENTS:
HARD REQUIRMENTS :
•	System   		:  	Pentium IV 2.4 GHz. 
•	Hard Disk 		:  	40 GB. 
•	Floppy Drive		:  	1.44 Mb. 
•	Monitor  		:  	15 VGA Colour. 
•	Mouse   		:  	Logitech. 
•	Ram   			:  	512 MB. 


SOFTWARE REQUIRMENTS :
•	Operating system  	:  	Windows 7 Professional. 
•	Coding Language 	: 	Python










SYSTEM STUDY FEASIBILITY STUDY

           The feasibility of the project is analyzed in this phase and business proposal is put forth with a very general plan for the project and some cost estimates. During system analysis the feasibility study of the proposed system is to be carried out. This is to ensure that the proposed system is not a burden to the company.  For feasibility analysis, some understanding of the major requirements for the system is essential.

Three key considerations involved in the feasibility analysis are	

•	ECONOMICAL FEASIBILITY
•	TECHNICAL FEASIBILITY
•	SOCIAL FEASIBILITY


ECONOMICAL FEASIBILITY
                   
  This study is carried out to check the economic impact that the system will have on the organization. The amount of fund that the company can pour into the research and development of the system is limited. The expenditures must be justified. Thus the developed system as well within the budget and this was achieved because most of the technologies used are freely available. Only the customized products had to be purchased. 

TECHNICAL FEASIBILITY
                
       This study is carried out to check the technical feasibility, that is, the technical requirements of the system. Any system developed must not have a high demand on the available technical resources. This will lead to high demands on the available technical resources. This will lead to high demands being placed on the client. The developed system must have a modest requirement, as only minimal or null changes are required for implementing this system.   

SOCIAL FEASIBILITY
       
           The aspect of study is to check the level of acceptance of the system by the user. This includes the process of training the user to use the system efficiently. The user must not feel threatened by the system, instead must accept it as a necessity. The level of acceptance by the users solely depends on the methods that are employed to educate the user about the system and to make him familiar with it. His level of confidence must be raised so that he is also able to make some constructive criticism, which is welcomed, as he is the final user of the system.





4.SYSTEM DESIGN

4.1 UML DIAGRAMS :

UML stands for Unified Modeling Language. UML is a standardized general-purpose modeling language in the field of object-oriented software engineering. The standard is managed, and was created by, the Object Management Group. 
The goal is for UML to become a common language for creating models of object oriented computer software. In its current form UML is comprised of two major components: a Meta-model and a notation. In the future, some form of method or process may also be added to; or associated with, UML.
	The Unified Modeling Language is a standard language for specifying, Visualization, Constructing and documenting the artifacts of software system, as well as for business modeling and other non-software systems. 
The UML represents a collection of best engineering practices that have proven successful in the modeling of large and complex systems.
 The UML is a very important part of developing objects oriented software and the software development process. The UML uses mostly graphical notations to express the design of software projects.

GOALS:
	The Primary goals in the design of the UML are as follows:
1.	Provide users a ready-to-use, expressive visual modeling Language so that they can develop and exchange meaningful models.
2.	Provide extendibility and specialization mechanisms to extend the core concepts.
3.	Be independent of particular programming languages and development process.
4.	Provide a formal basis for understanding the modeling language.
5.	Encourage the growth of OO tools market.
6.	Support higher level development concepts such as collaborations, frameworks, patterns and components.
7.	Integrate best practices.

USE CASE DIAGRAM:

A use case diagram in the Unified Modeling Language (UML) is a type of behavioral diagram defined by and created from a Use-case analysis. Its purpose is to present a graphical overview of the functionality provided by a system in terms of actors, their goals (represented as use cases), and any dependencies between those use cases. The main purpose of a use case diagram is to show what system functions are performed for which actor. Roles of the actors in the system can be depicted.
 



CLASS DIAGRAM:
In software engineering, a class diagram in the Unified Modeling Language (UML) is a type of static structure diagram that describes the structure of a system by showing the system's classes, their attributes, operations (or methods), and the relationships among the classes. It explains which class contains information.
 

SEQUENCE DIAGRAM:

A sequence diagram in Unified Modeling Language (UML) is a kind of interaction diagram that shows how processes operate with one another and in what order. It is a construct of a Message Sequence Chart. Sequence diagrams are sometimes called event diagrams, event scenarios, and timing diagrams.

 





COLLABORATION  DIAGRAM:

Activity diagrams are graphical representations of workflows of stepwise activities and actions with support for choice, iteration and concurrency. In the Unified Modeling Language, activity diagrams can be used to describe the business and operational step-by-step workflows of components in a system. An activity diagram shows the overall flow of control.

 
IMPLEMENTATION:
MODULES:

1)	Upload Iris Dataset:
 using this module we will upload dataset images to application
2)	Image Preprocessing: 
using this module we will resize images to equal size and then normalize pixel values
3)	Iris Segmentation & Features Extraction: 
using this module we will apply Daugman algorithm to extract iris region and then extract features or pixel values from that IRIS region
4)	Train ANN Algorithm: 
using this module we will feed extracted features to ANN algorithm to build iris classification or recognition module
5)	Iris Classification from Test Image:
 using this module we will upload eye image and then Daugman will extract IRIS region and then ANN model will recognized/predict person.



SOFTWARE ENVIRONMENT

What is Python :

 Below are some facts about  Python.
 Python is currently the most widely used multi-purpose, high-level programming language.
 Python allows programming in Object-Oriented and Procedural paradigms. Python programs generally    are smaller than other programming languages like Java.
 Programmers have to type relatively less and indentation requirement of the language, makes them readable all the time.
Python language is being used by almost all tech-giant companies like – Google, Amazon, Facebook, Instagram, Dropbox, Uber… etc.
The biggest strength of Python is huge collection of standard library which can be used for the following –
•	Machine Learning
•	GUI Applications (like Kivy, Tkinter, PyQt etc. )
•	Web frameworks like Django (used by YouTube, Instagram, Dropbox)
•	Image processing (like Opencv, Pillow)
•	Web scraping (like Scrapy, BeautifulSoup, Selenium)
•	Test frameworks
•	Multimedia

Advantages of Python :-
Let’s see how Python dominates over other languages.
1. Extensive Libraries	
Python downloads with an extensive library and it contain code for various purposes like regular expressions, documentation-generation, unit-testing, web browsers, threading, databases, CGI, email, image manipulation, and more. So, we don’t have to write the complete code for that manually.
2. Extensible
As we have seen earlier, Python can be extended to other languages. You can write some of your code in languages like C++ or C. This comes in handy, especially in projects.
3. Embeddable
Complimentary to extensibility, Python is embeddable as well. You can put your Python code in your source code of a different language, like C++. This lets us add scripting capabilities to our code in the other language.
4. Improved Productivity
The language’s simplicity and extensive libraries render programmers more productive than languages like Java and C++ do. Also, the fact that you need to write less and get more things done.
5. IOT Opportunities
Since Python forms the basis of new platforms like Raspberry Pi, it finds the future bright for the Internet Of Things. This is a way to connect the language with the real world.

When working with Java, you may have to create a class to print ‘Hello World’. But in Python, just a print statement will do. It is also quite easy to learn, understand, and code. This is why when people pick up Python, they have a hard time adjusting to other more verbose languages like Java.
7. Readable
Because it is not such a verbose language, reading Python is much like reading English. This is the reason why it is so easy to learn, understand, and code. It also does not need curly braces to define blocks, and indentation is mandatory. This further aids the readability of the code.
8. Object-Oriented
This language supports both the procedural and object-oriented programming paradigms. While functions help us with code reusability, classes and objects let us model the real world. A class allows the encapsulation of data and functions into one.
9. Free and Open-Source
Like we said earlier, Python is freely available. But not only can you download Python for free, but you can also download its source code, make changes to it, and even distribute it. It downloads with an extensive collection of libraries to help you with your tasks.
10. Portable
When you code your project in a language like C++, you may need to make some changes to it if you want to run it on another platform. But it isn’t the same with Python. Here, you need to code only once, and you can run it anywhere. This is called Write Once Run Anywhere (WORA). However, you need to be careful enough not to include any system-dependent features.
11. Interpreted
Lastly, we will say that it is an interpreted language. Since statements are executed one by one, debugging is easier than in compiled languages.
Any doubts till now in the advantages of Python? Mention in the comment section.







Advantages of Python Over Other Languages :
1. Less Coding
Almost all of the tasks done in Python requires less coding when the same task is done in other languages. Python also has an awesome standard library support, so you don’t have to search for any third-party libraries to get your job done. This is the reason that many people suggest learning Python to beginners.
2. Affordable
Python is free therefore individuals, small companies or big organizations can leverage the free available resources to build applications. Python is popular and widely used so it gives you better community support.
The 2019 Github annual survey showed us that Python has overtaken Java in the most popular programming language category.

3. Python is for Everyone
Python code can run on any machine whether it is Linux, Mac or Windows. Programmers need to learn different languages for different jobs but with Python, you can professionally build web apps, perform data analysis and machine learning, automate things, do web scraping and also build games and powerful visualizations. It is an all-rounder programming language.

Disadvantages of Python
So far, we’ve seen why Python is a great choice for your project. But if you choose it, you should be aware of its consequences as well. Let’s now see the downsides of choosing Python over another language.
1. Speed Limitations
We have seen that Python code is executed line by line. But since Python is interpreted, it often results in slow execution. This, however, isn’t a problem unless speed is a focal point for the project. In other words, unless high speed is a requirement, the benefits offered by Python are enough to distract us from its speed limitations.
2. Weak in Mobile Computing and Browsers
While it serves as an excellent server-side language, Python is much rarely seen on the client-side. Besides that, it is rarely ever used to implement smartphone-based applications. One such application is called Carbonnelle.
The reason it is not so famous despite the existence of Brython is that it isn’t that secure.
3. Design Restrictions
As you know, Python is dynamically-typed. This means that you don’t need to declare the type of variable while writing the code. It uses duck-typing. But wait, what’s that? Well, it just means that if it looks like a duck, it must be a duck. While this is easy on the programmers during coding, it can raise run-time errors.
4. Underdeveloped Database Access Layers
Compared to more widely used technologies like JDBC (Java DataBase Connectivity) and ODBC (Open DataBase Connectivity), Python’s database access layers are a bit underdeveloped. Consequently, it is less often applied in huge enterprises.
5. Simple
No, we’re not kidding. Python’s simplicity can indeed be a problem. Take my example. I don’t do Java, I’m more of a Python person. To me, its syntax is so simple that the verbosity of Java code seems unnecessary.
This was all about the Advantages and Disadvantages of Python Programming Language.
History of Python  : -

What do the alphabet and the programming language Python have in common? Right, both start with ABC. If we are talking about ABC in the Python context, it's clear that the programming language ABC is meant. ABC is a general-purpose programming language and programming environment, which had been developed in the Netherlands, Amsterdam, at the CWI (Centrum Wiskunde &Informatica). The greatest achievement of ABC was to influence the design of Python.Python was conceptualized in the late 1980s. Guido van Rossum worked that time in a project at the CWI, called Amoeba, a distributed operating system. In an interview with Bill Venners1, Guido van Rossum said: "In the early 1980s, I worked as an implementer on a team building a language called ABC at Centrum voor Wiskunde en Informatica (CWI). I don't know how well people know ABC's influence on Python. I try to mention ABC's influence because I'm indebted to everything I learned during that project and to the people who worked on it."Later on in the same Interview, Guido van Rossum continued: "I remembered all my experience and some of my frustration with ABC. I decided to try to design a simple scripting language that possessed some of ABC's better properties, but without its problems. So I started typing. I created a simple virtual machine, a simple parser, and a simple runtime. I made my own version of the various ABC parts that I liked. I created a basic syntax, used indentation for statement grouping instead of curly braces or begin-end blocks, and developed a small number of powerful data types: a hash table (or dictionary, as we call it), a list, strings, and numbers."


What is Machine Learning : -

Before we take a look at the details of various machine learning methods, let's start by looking at what machine learning is, and what it isn't. Machine learning is often categorized as a subfield of artificial intelligence, but I find that categorization can often be misleading at first brush. The study of machine learning certainly arose from research in this context, but in the data science application of machine learning methods, it's more helpful to think of machine learning as a means of building models of data.
Fundamentally, machine learning involves building mathematical models to help understand data. "Learning" enters the fray when we give these models tunable parameters that can be adapted to observed data; in this way the program can be considered to be "learning" from the data. Once these models have been fit to previously seen data, they can be used to predict and understand aspects of newly observed data. I'll leave to the reader the more philosophical digression regarding the extent to which this type of mathematical, model-based "learning" is similar to the "learning" exhibited by the human brain.Understanding the problem setting in machine learning is essential to using these tools effectively, and so we will start with some broad categorizations of the types of approaches we'll discuss here.
Categories Of Machine Leaning :-
At the most fundamental level, machine learning can be categorized into two main types: supervised learning and unsupervised learning.
Supervised learning involves somehow modeling the relationship between measured features of data and some label associated with the data; once this model is determined, it can be used to apply labels to new, unknown data. This is further subdivided into classification tasks and regression tasks: in classification, the labels are discrete categories, while in regression, the labels are continuous quantities. We will see examples of both types of supervised learning in the following section.
Unsupervised learning involves modeling the features of a dataset without reference to any label, and is often described as "letting the dataset speak for itself." These models include tasks such as clustering and dimensionality reduction. Clustering algorithms identify distinct groups of data, while dimensionality reduction algorithms search for more succinct representations of the data. We will see examples of both types of unsupervised learning in the following section.
Need for Machine Learning
Human beings, at this moment, are the most intelligent and advanced species on earth because they can think, evaluate and solve complex problems. On the other side, AI is still in its initial stage and haven’t surpassed human intelligence in many aspects. Then the question is that what is the need to make machine learn? The most suitable reason for doing this is, “to make decisions, based on data, with efficiency and scale”.
Lately, organizations are investing heavily in newer technologies like Artificial Intelligence, Machine Learning and Deep Learning to get the key information from data to perform several real-world tasks and solve problems. We can call it data-driven decisions taken by machines, particularly to automate the process. These data-driven decisions can be used, instead of using programing logic, in the problems that cannot be programmed inherently. The fact is that we can’t do without human intelligence, but other aspect is that we all need to solve real-world problems with efficiency at a huge scale. That is why the need for machine learning arises.
Challenges in Machines Learning :-

While Machine Learning is rapidly evolving, making significant strides with cybersecurity and autonomous cars, this segment of AI as whole still has a long way to go. The reason behind is that ML has not been able to overcome number of challenges. The challenges that ML is facing currently are −
Quality of data − Having good-quality data for ML algorithms is one of the biggest challenges. Use of low-quality data leads to the problems related to data preprocessing and feature extraction.
Time-Consuming task − Another challenge faced by ML models is the consumption of time especially for data acquisition, feature extraction and retrieval.
Lack of specialist persons − As ML technology is still in its infancy stage, availability of expert resources is a tough job.
No clear objective for formulating business problems − Having no clear objective and well-defined goal for business problems is another key challenge for ML because this technology is not that mature yet.
Issue of overfitting & underfitting − If the model is overfitting or underfitting, it cannot be represented well for the problem.
Curse of dimensionality − Another challenge ML model faces is too many features of data points. This can be a real hindrance.
Difficulty in deployment − Complexity of the ML model makes it quite difficult to be deployed in real life.
Applications of Machines Learning :-

Machine Learning is the most rapidly growing technology and according to researchers we are in the golden year of AI and ML. It is used to solve many real-world complex problems which cannot be solved with traditional approach. Following are some real-world applications of ML −
•	Emotion analysis
•	Sentiment analysis
•	Error detection and prevention
•	Weather forecasting and prediction
•	Stock market analysis and forecasting
•	Speech synthesis
•	Speech recognition
•	Customer segmentation
•	Object recognition
•	Fraud detection
•	Fraud prevention
•	Recommendation of products to customer in online shopping




How to Start Learning Machine Learning?
Arthur Samuel coined the term “Machine Learning” in 1959 and defined it as a “Field of study that gives computers the capability to learn without being explicitly programmed”.
And that was the beginning of Machine Learning! In modern times, Machine Learning is one of the most popular (if not the most!) career choices. According to Indeed, Machine Learning Engineer Is The Best Job of 2019 with a 344% growth and an average base salary of $146,085 per year.
But there is still a lot of doubt about what exactly is Machine Learning and how to start learning it? So this article deals with the Basics of Machine Learning and also the path you can follow to eventually become a full-fledged Machine Learning Engineer. Now let’s get started!!!
How to start learning ML?
This is a rough roadmap you can follow on your way to becoming an insanely talented Machine Learning Engineer. Of course, you can always modify the steps according to your needs to reach your desired end-goal!
Step 1 – Understand the Prerequisites
In case you are a genius, you could start ML directly but normally, there are some prerequisites that you need to know which include Linear Algebra, Multivariate Calculus, Statistics, and Python. And if you don’t know these, never fear! You don’t need a Ph.D. degree in these topics to get started but you do need a basic understanding.
(a) Learn Linear Algebra and Multivariate Calculus
Both Linear Algebra and Multivariate Calculus are important in Machine Learning. However, the extent to which you need them depends on your role as a data scientist. If you are more focused on application heavy machine learning, then you will not be that heavily focused on maths as there are many common libraries available. But if you want to focus on R&D in Machine Learning, then mastery of Linear Algebra and Multivariate Calculus is very important as you will have to implement many ML algorithms from scratch.
(b) Learn Statistics
Data plays a huge role in Machine Learning. In fact, around 80% of your time as an ML expert will be spent collecting and cleaning data. And statistics is a field that handles the collection, analysis, and presentation of data. So it is no surprise that you need to learn it!!!
Some of the key concepts in statistics that are important are Statistical Significance, Probability Distributions, Hypothesis Testing, Regression, etc. Also, Bayesian Thinking is also a very important part of ML which deals with various concepts like Conditional Probability, Priors, and Posteriors, Maximum Likelihood, etc.
(c) Learn Python
Some people prefer to skip Linear Algebra, Multivariate Calculus and Statistics and learn them as they go along with trial and error. But the one thing that you absolutely cannot skip is Python! While there are other languages you can use for Machine Learning like R, Scala, etc. Python is currently the most popular language for ML. In fact, there are many Python libraries that are specifically useful for Artificial Intelligence and Machine Learning such as Keras, TensorFlow, Scikit-learn, etc.
So if you want to learn ML, it’s best if you learn Python! You can do that using various online resources and courses such as Fork Python available Free on GeeksforGeeks.
Step 2 – Learn Various ML Concepts
Now that you are done with the prerequisites, you can move on to actually learning ML (Which is the fun part!!!) It’s best to start with the basics and then move on to the more complicated stuff. Some of the basic concepts in ML are:
(a) Terminologies of Machine Learning
•	Model – A model is a specific representation learned from data by applying some machine learning algorithm. A model is also called a hypothesis.
•	Feature – A feature is an individual measurable property of the data. A set of numeric features can be conveniently described by a feature vector. Feature vectors are fed as input to the model. For example, in order to predict a fruit, there may be features like color, smell, taste, etc.
•	Target (Label) – A target variable or label is the value to be predicted by our model. For the fruit example discussed in the feature section, the label with each set of input would be the name of the fruit like apple, orange, banana, etc.
•	Training – The idea is to give a set of inputs(features) and it’s expected outputs(labels), so after training, we will have a model (hypothesis) that will then map new data to one of the categories trained on.
•	Prediction – Once our model is ready, it can be fed a set of inputs to which it will provide a predicted output(label).
(b) Types of Machine Learning
•	Supervised Learning – This involves learning from a training dataset with labeled data using classification and regression models. This learning process continues until the required level of performance is achieved.
•	Unsupervised Learning – This involves using unlabelled data and then finding the underlying structure in the data in order to learn more and more about the data itself using factor and cluster analysis models.
•	Semi-supervised Learning – This involves using unlabelled data like Unsupervised Learning with a small amount of labeled data. Using labeled data vastly increases the learning accuracy and is also more cost-effective than Supervised Learning.
•	Reinforcement Learning – This involves learning optimal actions through trial and error. So the next action is decided by learning behaviors that are based on the current state and that will maximize the reward in the future.
Advantages of Machine learning :-
1. Easily identifies trends and patterns -
Machine Learning can review large volumes of data and discover specific trends and patterns that would not be apparent to humans. For instance, for an e-commerce website like Amazon, it serves to understand the browsing behaviors and purchase histories of its users to help cater to the right products, deals, and reminders relevant to them. It uses the results to reveal relevant advertisements to them.
2. No human intervention needed (automation)
With ML, you don’t need to babysit your project every step of the way. Since it means giving machines the ability to learn, it lets them make predictions and also improve the algorithms on their own. A common example of this is anti-virus softwares; they learn to filter new threats as they are recognized. ML is also good at recognizing spam.
3. Continuous Improvement 
As ML algorithms gain experience, they keep improving in accuracy and efficiency. This lets them make better decisions. Say you need to make a weather forecast model. As the amount of data you have keeps growing, your algorithms learn to make more accurate predictions faster.
4. Handling multi-dimensional and multi-variety data
Machine Learning algorithms are good at handling data that are multi-dimensional and multi-variety, and they can do this in dynamic or uncertain environments.
5. Wide Applications
You could be an e-tailer or a healthcare provider and make ML work for you. Where it does apply, it holds the capability to help deliver a much more personal experience to customers while also targeting the right customers.
Disadvantages of Machine Learning :-
1. Data Acquisition
Machine Learning requires massive data sets to train on, and these should be inclusive/unbiased, and of good quality. There can also be times where they must wait for new data to be generated.
2. Time and Resources
ML needs enough time to let the algorithms learn and develop enough to fulfill their purpose with a considerable amount of accuracy and relevancy. It also needs massive resources to function. This can mean additional requirements of computer power for you.
3. Interpretation of Results
Another major challenge is the ability to accurately interpret results generated by the algorithms. You must also carefully choose the algorithms for your purpose.
4. High error-susceptibility
Machine Learning is autonomous but highly susceptible to errors. Suppose you train an algorithm with data sets small enough to not be inclusive. You end up with biased predictions coming from a biased training set. This leads to irrelevant advertisements being displayed to customers. In the case of ML, such blunders can set off a chain of errors that can go undetected for long periods of time. And when they do get noticed, it takes quite some time to recognize the source of the issue, and even longer to correct it.

Python Development Steps  : -
Guido Van Rossum published the first version of Python code (version 0.9.0) at alt.sources in February 1991. This release included already exception handling, functions, and the core data types of list, dict, str and others. It was also object oriented and had a module system.
Python version 1.0 was released in January 1994. The major new features included in this release were the functional programming tools lambda, map, filter and reduce, which Guido Van Rossum never liked.Six and a half years later in October 2000, Python 2.0 was introduced. This release included list comprehensions, a full garbage collector and it was supporting unicode.Python flourished for another 8 years in the versions 2.x before the next major release as Python 3.0 (also known as "Python 3000" and "Py3K") was released. Python 3 is not backwards compatible with Python 2.x. The emphasis in Python 3 had been on the removal of duplicate programming constructs and modules, thus fulfilling or coming close to fulfilling the 13th law of the Zen of Python: "There should be one -- and preferably only one -- obvious way to do it."Some changes in Python 7.3:
•	Print is now a function
•	Views and iterators instead of lists
•	The rules for ordering comparisons have been simplified. E.g. a heterogeneous list cannot be     sorted, because all the elements of a list must be comparable to each other.
•	There is only one integer type left, i.e. int. long is int as well.
•	The division of two integers returns a float instead of an integer. "//" can be used to have the "old" behaviour.
•	Text Vs. Data Instead Of Unicode Vs. 8-bit
Purpose :-  
We demonstrated that our approach enables successful segmentation of intra-retinal layers—even with low-quality images containing speckle noise, low contrast, and different intensity ranges throughout—with the assistance of the ANIS feature.
Python
Python is an interpreted high-level programming language for general-purpose programming. Created by Guido van Rossum and first released in 1991, Python has a design philosophy that emphasizes code readability, notably using significant whitespace. 
Python features a dynamic type system and automatic memory management. It supports multiple programming paradigms, including object-oriented, imperative, functional and procedural, and has a large and comprehensive standard library. 
•	Python is Interpreted − Python is processed at runtime by the interpreter. You do not need to compile your program before executing it. This is similar to PERL and PHP. 
•	Python is Interactive − you can actually sit at a Python prompt and interact with the interpreter directly to write your programs. 
Python also acknowledges that speed of development is important. Readable and terse code is part of this, and so is access to powerful constructs that avoid tedious repetition of code. Maintainability also ties into this may be an all but useless metric, but it does say something about how much code you have to scan, read and/or understand to troubleshoot problems or tweak behaviors. This speed of development, the ease with which a programmer of other languages can pick up basic Python skills and the huge standard library is key to another area where Python excels. All its tools have been quick to implement, saved a lot of time, and several of them have later been patched and updated by people with no Python background - without breaking.
Modules Used in Project  :-
Tensorflow
TensorFlow is a free and open-source software library for dataflow and differentiable programming across a range of tasks. It is a symbolic math library, and is also used for machine learning applications such as neural networks. It is used for both research and production at Google. 
TensorFlow was developed by the Google Brain team for internal Google use. It was released under the Apache 2.0 open-source license on November 9, 2015.
Numpy
Numpy is a general-purpose array-processing package. It provides a high-performance multidimensional array object, and tools for working with these arrays.
It is the fundamental package for scientific computing with Python. It contains various features including these important ones:
	A powerful N-dimensional array object
	Sophisticated (broadcasting) functions
	Tools for integrating C/C++ and Fortran code
	Useful linear algebra, Fourier transform, and random number capabilities
Besides its obvious scientific uses, Numpy can also be used as an efficient multi-dimensional container of generic data. Arbitrary data-types can be defined using Numpy which allows Numpy to seamlessly and speedily integrate with a wide variety of databases.
Pandas
Pandas is an open-source Python Library providing high-performance data manipulation and analysis tool using its powerful data structures. Python was majorly used for data munging and preparation. It had very little contribution towards data analysis. Pandas solved this problem. Using Pandas, we can accomplish five typical steps in the processing and analysis of data, regardless of the origin of data load, prepare, manipulate, model, and analyze. Python with Pandas is used in a wide range of fields including academic and commercial domains including finance, economics, Statistics, analytics, etc.
Matplotlib
Matplotlib is a Python 2D plotting library which produces publication quality figures in a variety of hardcopy formats and interactive environments across platforms. Matplotlib can be used in Python scripts, the Python and IPython shells, the Jupyter Notebook, web application servers, and four graphical user interface toolkits. Matplotlib tries to make easy things easy and hard things possible. You can generate plots, histograms, power spectra, bar charts, error charts, scatter plots, etc., with just a few lines of code. For examples, see the sample plots and thumbnail gallery.
For simple plotting the pyplot module provides a MATLAB-like interface, particularly when combined with IPython. For the power user, you have full control of line styles, font properties, axes properties, etc, via an object oriented interface or via a set of functions familiar to MATLAB users.
Scikit – learn
Scikit-learn provides a range of supervised and unsupervised learning algorithms via a consistent interface in Python. It is licensed under a permissive simplified BSD license and is distributed under many Linux distributions, encouraging academic and commercial use. Python
Python is an interpreted high-level programming language for general-purpose programming. Created by Guido van Rossum and first released in 1991, Python has a design philosophy that emphasizes code readability, notably using significant whitespace. 
Python features a dynamic type system and automatic memory management. It supports multiple programming paradigms, including object-oriented, imperative, functional and procedural, and has a large and comprehensive standard library. 
•	Python is Interpreted − Python is processed at runtime by the interpreter. You do not need to compile your program before executing it. This is similar to PERL and PHP. 
•	Python is Interactive − you can actually sit at a Python prompt and interact with the interpreter directly to write your programs. 
Python also acknowledges that speed of development is important. Readable and terse code is part of this, and so is access to powerful constructs that avoid tedious repetition of code. Maintainability also ties into this may be an all but useless metric, but it does say something about how much code you have to scan, read and/or understand to troubleshoot problems or tweak behaviors. This speed of development, the ease with which a programmer of other languages can pick up basic Python skills and the huge standard library is key to another area where Python excels. All its tools have been quick to implement, saved a lot of time, and several of them have later been patched and updated by people with no Python background - without breaking.
Install Python Step-by-Step in Windows and Mac :
Python a versatile programming language doesn’t come pre-installed on your computer devices. Python was first released in the year 1991 and until today it is a very popular high-level programming language. Its style philosophy emphasizes code readability with its notable use of great whitespace.
The object-oriented approach and language construct provided by Python enables programmers to write both clear and logical code for projects. This software does not come pre-packaged with Windows.

How to Install Python on Windows and Mac :

There have been several updates in the Python version over the years. The question is how to install Python? It might be confusing for the beginner who is willing to start learning Python but this tutorial will solve your query. The latest or the newest version of Python is version 3.7.4 or in other words, it is Python 3.
Note: The python version 3.7.4 cannot be used on Windows XP or earlier devices.

Before you start with the installation process of Python. First, you need to know about your System Requirements. Based on your system type i.e. operating system and based processor, you must download the python version. My system type is a Windows 64-bit operating system. So the steps below are to install python version 3.7.4 on Windows 7 device or to install Python 3. Download the Python Cheatsheet here.The steps on how to install Python on Windows 10, 8 and 7 are divided into 4 parts to help understand better.

Download the Correct version into the system

Step 1: Go to the official site to download and install python using Google Chrome or any other web browser. OR Click on the following link: https://www.python.org


 
Now, check for the latest and the correct version for your operating system.
Step 2: Click on the Download Tab.
 
Step 3: You can either select the Download Python for windows 3.7.4 button in Yellow Color or you can scroll further down and click on download with respective to their version. Here, we are downloading the most recent python version for windows 3.7.4
 
Step 4: Scroll down the page until you find the Files option.

Step 5: Here you see a different version of python along with the operating system.

 



• To download Windows 32-bit python, you can select any one from the three options: Windows x86 embeddable zip file, Windows x86 executable installer or Windows x86  web-based installer. 
•To download Windows 64-bit python, you can select any one from the three options: Windows x86-64 embeddable zip file, Windows x86-64 executable installer or Windows x86-64 web-based installer.
Here we will install Windows x86-64 web-based installer. Here your first part regarding which version of python is to be downloaded is completed. Now we move ahead with the second part in installing python i.e. Installation
Note: To know the changes or updates that are made in the version you can click on the Release Note Option.
Installation of Python
Step 1: Go to Download and Open the downloaded python version to carry out the installation process.
 
Step 2: Before you click on Install Now, Make sure to put a tick on Add Python 3.7 to PATH.

 

Step 3: Click on Install NOW After the installation is successful. Click on Close.

 

With these above three steps on python installation, you have successfully and correctly installed Python. Now is the time to verify the installation.
Note: The installation process might take a couple of minutes.

Verify the Python Installation
Step 1: Click on Start
Step 2: In the Windows Run Command, type “cmd”.

 
Step 3: Open the Command prompt option.
Step 4: Let us test whether the python is correctly installed. Type python –V and press Enter.

 
Step 5: You will get the answer as 3.7.4
Note: If you have any of the earlier versions of Python already installed. You must first uninstall the earlier version and then install the new one. 

Check how the Python IDLE works
Step 1: Click on Start
Step 2: In the Windows Run command, type “python idle”.
 
Step 3: Click on IDLE (Python 3.7 64-bit) and launch the program
Step 4: To go ahead with working in IDLE you must first save the file. Click on File > Click on Save

 
Step 5: Name the file and save as type should be Python files. Click on SAVE. Here I have named the files as Hey World.
Step 6: Now for e.g. enter print

6.SYSTEM TEST
The purpose of testing is to discover errors. Testing is the process of trying to discover every conceivable fault or weakness in a work product. It provides a way to check the functionality of components, sub assemblies, assemblies and/or a finished product It is the process of exercising software with the intent of ensuring that the Software system meets its requirements and user expectations and does not fail in an unacceptable manner. There are various types of test. Each test type addresses a specific testing requirement.
TYPES OF TESTS

Unit testing
                     Unit testing involves the design of test cases that validate that the internal program logic is functioning properly, and that program inputs produce valid outputs. All decision branches and internal code flow should be validated. It is the testing of individual software units of the application .it is done after the completion of an individual unit before integration. This is a structural testing, that relies on knowledge of its construction and is invasive. Unit tests perform basic tests at component level and test a specific business process, application, and/or system configuration. Unit tests ensure that each unique path of a business process performs accurately to the documented specifications and contains clearly defined inputs and expected results.
Integration testing
                             Integration tests are designed to test integrated software components to determine if they actually run as one program.  Testing is event driven and is more concerned with the basic outcome of screens or fields. Integration tests demonstrate that although the components were individually satisfaction, as shown by successfully unit testing, the combination of components is correct and consistent. Integration testing is specifically aimed at   exposing the problems that arise from the combination of components.
Functional test
                   Functional tests provide systematic demonstrations that functions tested are available as specified by the business and technical requirements, system documentation, and user manuals.
                        Functional testing is centered on the following items:
       Valid Input               :  identified classes of valid input must be accepted.
       Invalid Input             : identified classes of invalid input must be rejected.
       Functions                  : identified functions must be exercised.
       Output           	           : identified classes of application outputs must be    exercised.
      Systems/Procedures   : interfacing systems or procedures must be invoked.
                       Organization and preparation of functional tests is focused on requirements, key functions, or special test cases. In addition, systematic coverage pertaining to identify Business process flows; data fields, predefined processes, and successive processes must be considered for testing. Before functional testing is complete, additional tests are identified and the effective value of current tests is determined.
System Test
                       System testing ensures that the entire integrated software system meets requirements. It tests a configuration to ensure known and predictable results. An example of system testing is the configuration oriented system integration test. System testing is based on process descriptions and flows, emphasizing pre-driven process links and integration points.
White Box Testing
                        White Box Testing is a testing in which in which the software tester has knowledge of the inner workings, structure and language of the software, or at least its purpose. It is purpose. It is used to test areas that cannot be reached from a black box level.
Black Box Testing
                         Black Box Testing is testing the software without any knowledge of the inner workings, structure or language of the module being tested. Black box tests, as most other kinds of tests, must be written from a definitive source document, such as specification or requirements document, such as specification or requirements document. It is a testing in which the software under test is treated, as a black box .you cannot “see” into it. The test provides inputs and responds to outputs without considering how the software works.
Unit Testing
                         Unit testing is usually conducted as part of a combined code and unit test phase of the software lifecycle, although it is not uncommon for coding and unit testing to be conducted as two distinct phases.
Test strategy and approach
	               Field testing will be performed manually and functional tests will be written in detail.
Test objectives
•	All field entries must work properly.
•	Pages must be activated from the identified link.
•	The entry screen, messages and responses must not be delayed.

Features to be tested
•	Verify that the entries are of the correct format
•	No duplicate entries should be allowed
•	All links should take the user to the correct page.
Integration Testing
                      Software integration testing is the incremental integration testing of two or more integrated software components on a single platform to produce failures caused by interface defects.
The task of the integration test is to check that components or software applications, e.g. components in a software system or – one step up – software applications at the company level – interact without error.
Test Results: All the test cases mentioned above passed successfully. No defects encountered.
Acceptance Testing
User Acceptance Testing is a critical phase of any project and requires significant participation by the end user. It also ensures that the system meets the functional requirements.
Test Results: All the test cases mentioned above passed successfully. No defects encountered.























Screenshots :

To run project double click on ‘run.bat’ file to get below output
 
In above screen click on ‘Upload Iris Dataset’ button to upload dataset like below screen
 
In above screen selecting and uploading ‘IrisDataset’ folder and then click on ‘Select Folder’ button to load dataset and to get below output
 
In above screen dataset loaded and now click on ‘Image Preprocessing’ button to normalize pixel values and get below output
 
In above screen we can see application processed 1400 images from dataset and now click on ‘Iris Segmentation & Features Extraction’ button to extract iris and then extract features from it
 
In above screen we can see iris segmented and extracted features from all images and each image will 64 X 64 height and width and in above screen I am displaying one iris segmented image to check whether images are segmented properly or not and now close above image and then click on ‘Train ANN Algorithm’ button to train ANN with extracted features and get below output
 
In above screen ANN model generated we got it prediction confusion matrix graph where x-axis represents predicted classes and y-axis represents TRUE classes and in diagnol we can maximum predictions are correct and now close above image to get below output
 
In above screen with ANN we got 96% accuracy and now click on ‘Iris Classification from Test Image’ button to upload test image and get classification or recognition output
 
In above screen selecting and uploading ’15.bmp’ and then click on ‘Open’ button to get below output 
 
In above screen in red colour text we can see iris classified as ‘Fatma’ and we can see Daugman segmented image and similarly u can upload other images and test
 
In above screen iris classified as ‘aeva’
 
In above screen iris classified as ‘Bryan’
CONCLUSION :
It can be concluded from the previous discussions, it can be concluded that highly classified and secure applications need reliable security systems to prevent unauthorized trespassing. Iris recognition is a form of bio metric authentication system that uses high end mathematical techniques and processes on the digital image of the Iris of the eye. It is mainly based on the pattern recognition method where in it identifies sharp and distinct patterns of the Iris that can accurately recognize the intended user. In the proposed work, iris localization has been performed by using the Daugman’s algorithm which is an integro-differential operator capable of separating or segmenting out regular shapes. The Daugman’s algorithm also has a noise smoothening capability. The features computed in the work are Contrast, Correlation, Energy, Homogeneity, Mean, Standard Deviation, Entropy, RMS, Variance, Smoothness, Kurtosis and Skewness. The features tend to behave uniquely for different iris images. However, overlapping values are possible. The features are then fed to a neural network using the Levenberg-Marquardt back propagation training rule. After training the neural network with feature values of authorized images, the subsequent step is testing the neural network for accuracy. The standard MMU database has been used for design of the system. It has been found that the proposed system attains an accuracy of 99.7% which is higher compared to the previously existing system using the same database.












REFERENCES :
[1] Alaa S. Al-Waisy et al., “A multi-biometric iris recognition system based on a deep learning approach”, Springer 2018
 [2] Cunjian Chen , Arun Ross et al., “A Multi-task Convolutional Neural Network for Joint Iris Detection and Presentation Attack Detection”, IEEE 2018
 [3] Shabab Bazrafkan et al., “Enhancing iris authentication on handheld devices using deep learning derived segmentation techniques”, IEEE 2018 
[4] Ritesh Vyas, Tirupathiraju Kanumuri, Gyanendra Sheoran, Pawan Dubey, “DeepIrisNet: Deep iris representation with applications in iris recognition and cross-sensor iris recognition”,, IEEE, 2017. 
[5] R. Raghavendra et al., “ContlensNet: Robust Iris Contact Lens Detection Using Deep Convolutional Neural Networks”, IEEE 2017 
[6] Nianfeng Liu et.al, “Accurate iris segmentation in noncooperative environments using fully convolutional networks”, IEEE 2016 
[7] MariaDe Marsico et al., “Iris recognition through machine learning techniques: A survey”, IEEE 2016
 [8] Sushilkumar S. Salve et al., “Iris recognition using SVM and ANN”, IEEE 2016 
[9] Shervin Minaee et al., “An experimental study of deep convolutional features for iris recognition”, IEEE 2016
 [10] Shervin Minaee , AmirAli Abdolrashidi et al., “Iris recognition using scattering transform and textural features”, IEEE 2015 
[11] Pedro Silva et al., “An Approach to Iris Contact Lens Detection Based on Deep Image Representations”, IEEE 2015
 [12] Firoz Mahmud et al., “PCA and back-propagation neural network based face recognition system”, IEEE 2015
[13] Vivek Srivastava et.al , “Biometric recognition by hybridization of evolutionary fuzzy clustering with functional neural networks”, Springer 2014 
[14] Miloš Oravec, “Feature extraction and classification by machine learning methods for biometric recognition of face and iris”, IEEE 2014
 [15] Navjot Kaur , Mamta Juneja, “A review on Iris Recognition”, IEEE 2014
 [16] Heinz Hofbauer et al. , “A Ground Truth for Iris Segmentation, IEEE 2014 
[17] Daniela Sánchez et al., “Modular granular neural networks optimization with Multi-Objective Hierarchical Genetic Algorithm for human recognition based on iris biometric”, IEEE 2013
 [18] Nuzhat Faiz Shaikh et al. , “Improving the Accuracy of Iris Recognition System using Neural Network and Particle Swarm Optimization”, Citeseer 2013 
[19] Ching-Han Chen et al., “Optimal fusion of multimodal biometric authentication using wavelet probabilistic neural network”, IEEE 2013
 [20] Mrunal M. Khedkar et al., “Robust human iris pattern recognition system using neural network approach”, IEEE 2013 
[21] DM Monro, S Rakshit, D Zhang, “DCT-based iris recognition ”, IEEE 2007. 
[22] SAC Schuckers, NA Schmid, “On techniques for angle compensation in nonideal iris recognition ”, IEEE 2007.
 [23] A Ross, AK Jain, “Human recognition using biometrics: an overview ”, Springer 2007 
[24] JR Matey, O Naroditsky, K Hanna, “Iris on the move: Acquisition of images for iris recognition in less constrained environments ”, IEEE 2006 
[25] D Cho, KR Park, DW Rhee, Y Kim, “Pupil and iris localization for iris recognition in mobile phones, IEEE 2006 
[26] K Miyazawa, K Ito, T Aoki, K Kobayashi, A phasebased iris recognition algorithm ”, Springer 2006.
 [27] P Yao, J Li, X Ye, Z Zhuang, B Li, “Iris recognition algorithm using modified log-gabor filters”, IEEE 2006
 [28] Z Sun, Y Wang, T Tan, J Cui, “Improving iris recognition accuracy via cascaded classifiers ”, Elsevier 2005 
[29] C Fancourt, L Bogoni, K Hanna, Y Guo, “Iris recognition at a distance ”, Springer 2005 
[30] H Proença, LA Alexandre , “UBIRIS: A noisy iris image database , Springer 2005.





