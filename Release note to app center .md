# NYMU BMI translation of medicine stroke project (analysis center) <br>
Release note to app center <br>                              
Editor: Isa ko <br>
The aim of this file is to suggest how to design a questionnarire on the basis of our stroke model and also demonstrate how to use the equation given below in our app.

## Feature
Questionnarire should at least include these several features below 
feature	| content | range 
------|-----------|------------
gender|	1: male| 2: female	 
age	|numeric |	6 – 95 yrs <br>
SBP	numeric |	20 – 250 mmHg <br>
BMI	numeric	| 10 - 50 <br>
Hyperlipidemia_ornot |	0: No 1: yes	<br>
DM_ornot | 0: No 1: yes	<br>
drink_ornot	| 0: No 1: yes	<br>

## Equation 
There are 3 steps to get stroke probability: <br>
>Step 1: 
>*Importance scores= (-0.23)*[gender]+ 1.5*[age]+ 0.27*[SBP]+ 0.14*[BMI]+ 0.36*[Hyperlipidemia_ornot]+ 0.28*[DM_ornot]+ 0.08*[drink_ornot]- 0.028

>Step 2：
>*y = 0.0658* (Importance scores) - 7.522

>Step 3 :
>According to logistic regression model, probability should be transformed from sigmoid function:

![image](https://user-images.githubusercontent.com/69064353/115986356-5ad48080-a5e2-11eb-8a95-dca63b2d1bde.png)

## Stroke Probability: 
![image](https://user-images.githubusercontent.com/69064353/115986393-822b4d80-a5e2-11eb-8a72-e24afb96a889.png)


