# Benzyl-Alcohol-
Predictive modelling on aerobic oxidation of benzyl alcohol by ceria-based catalysts based on past research publications

Introduction.
Aerobic oxidation of benzyl alcohol is an important reaction from both academic and industrial point of views. Academically, benzyl alcohol gathers attention due to its high affinity towards oxidation and generation of non-enolizable aldehydes as products. It is often used as a probe reaction to evaluate the ability of catalysts toward oxidation of alcohols1,2. Industrially, its major oxidative product, benzaldehyde, is known as a versatile chemical ingredient in agrochemical, pharmaceutical, perfumery and many other fine chemical industries 3,4. Therefore, in recent years, a tremendous amount of works has been done to improvise the benzyl alcohol oxidation in terms of ambient reaction conditions, efficient catalyst designing and achievement of desired yield. 
However, reaction optimization is rather complicated procedure that depends on many different factors like nature of catalysts, solvents, reaction temperature, pressure, time duration etc. Moreover, the nature of catalysts is subject to further diverse factors like type of supports, particle size, use of promoters, surface area, morphology etc. As for example, the aerobic oxidation of benzyl alcohol have been studied with different supports like TiO2 5–8 CeO2 1,2,8–14, MnO24,15–17, active noble metals like Au1,2,9,10,13, Pd1,8,11,14, different metal promoters like  Bi2,9, Mn10, Sn18, Zr19 , different solvents like toluene9, cyclohexane19, water20 or without any solvent1,14 and at different pressure ranges like 0.1 MPa 9, 0.2 MPa 19 and 0.3 MPa1 .
In the presence of such wide range of variables, slight change in even one of those factors can highly influence the research results, in certain cases showing very different outcomes21. However, it is rather arduous to optimize all those parameters in a single experimental study. Therefore, most studies focus on some factors in a reaction, keeping the other factors constant. However, as the determining factors are interlinked, change in one factor might influence the other, therefore many fundamental aspects are overlooked.21 Even so, the wide range of experimental works done in the past can be used to generate predictive models to generate expectable outcomes of an unstudied condition.
In this work, statistical and data analysis models have been used to predict the outcome of different catalytic results of aerobic oxidation of benzyl alcohol using CeO2based catalysts.

2. Materials and Methods.
2.1. Data Extraction.
4 research publications1,9,11,19 on aerobic benzyl alcohol oxidation with CeO2based catalysts are taken and 70 datapoints are extracted. The different variables and factors in the datapoints are mentioned in Table 1


Table 1. Different Predictor Variables, Their Types, Ranges and Values
Variables	Variable Type	Range/Values	Output
Noble Metal
	Categorical	Au, Pd	









	Conversion of Benzyl Alcohol

	Yield of Benzaldehyde
Weight% of Noble Metals
	Continuous	0-2.5 %	
Particle Size of Noble Metals
	Continuous	0-6.4 nm	
Preparation Procedure of Noble Metals	Categorical	Deposition-Precipitation(DP), 

Wetness Impregnation (WI), 

Incipient Wetness Impregnation (IWI)	

Calcination Temperature of Noble Metal Nanoparticles	
Continuous	
298K – 973K	
Support (CeO2) Morphology	Categorical	Nanorods, nanocubes, nanopolyhedra, nanoparticles, mesoporous	

Metal Promoters	
Categorical	
Bi, Zr	
Mole Fraction of Metal Promoters
	Continuous	0-0.4	
Solvents	Categorical	Toluene, Cyclohexane, n-Heptane, Flurotoluene, 1,4-Dioxane, Methanol, Water, No-solvent	

Molar Concentration of Benzyl Alcohol	
Continuous	
1-9.62 M	
Reaction Temperature	Continuous	353-393K	

Reaction Pressure	
Continuous	
0.1-0.3 MPa	

Reaction Time	
Continuous	
0.25-6 hour	

	Computational Details. 

The statistical predictions were done using Classification Learner and Regression Learner applications in Matlab R2019a platform. K-fold cross validation was applied on the data, i.e. the data was divided into “k” number of subsets (here k =5), and the statistical models were applied on 4/5th of the data to generate a trained model. The trained model was then applied on the remaining 1/5th of the data to validate the predictions. The process was repeated k times (i.e. 5 times) to validate each subset. Initially all the classification and regression models were applied (including Regression Tree, Support Vector Machines, Linear Regression etc) to get the most accurate prediction of the morphology of support and the catalytic conversion. The values with high predication accuracy are reported.

	Results and Discussions.

	Prediction of Catalytic Conversion of Benzyl Alcohol

Different regression models were used to predict the percentage conversion of benzyl alcohol to benzaldehyde using the predctors/input variables described in Table 1. The RMSE (Root Mean Square Error) values show the closeness of actual datapoints to the predicted values. A low RMSE value shows more accurate prediction. The R2 values are used to estimate the good fit of the results in a particular model. The equations followed to determine the RMSE and R2 values are given below:

RMSE=〖( 1/n 〖∑_1^n▒〖 (p_i 〗- t_i)〗^2  )〗^(1/( 2))   ……………….Eq(1)

R^(2 )=1-  (∑_1^n▒(p_i-t_i )^2 )/(∑_1^n▒(t_i-t ⃑ )^2 )   ………………Eq (2)

Where pi and ti are predicted and actual values of percentage conversion of Benzyl Alcohol respectively, t ⃑ is the mean of ti values and n is the number of experiments.

The optimization of the Artificial Neural Networ model had shown R value of 0.96 and RMSE value of 7.72
	Estimation of the Relative Importance of Different Variables

   Table 2.              
Variable	RMSE without Variable	Difference in RMSE	
Noble Metals	33.95	26.23	
Metal Promoters	17.42	9.7	
Type of CeO2	30.00	22.28	
Solvents	32.36	24.64	
Volume of Solution	19.08	11.37	
Concentration of Benzyl Alcohol	13.56	5.85	
Reaction Time	37.76	30.04	
Reaction Temperature	167.7	160	
Catalyst Amount	17.67	9.95	

The relative importance of the catalyst properties and the operational variable is shown in Table 2. Reaction Temperature can be observed as the single most important factor, due to its long range of effect and fundamental importance in reaction kinetics21. The reaction time also had shown high significance, however, its effect was observed to be substantially less than the reaction temperature, probably because effective reaction time is dependent on many other factors like the nature of the catalysts or other operational variables, which share the predictability of the outcome in a manner similar to the reaction time. 





References.
(1) 	Li, X.; Feng, J.; Perdjon, M.; Oh, R.; Zhao, W.; Huang, X.; Liu, S. Investigations of Supported Au-Pd Nanoparticles on Synthesized CeO2 with Different Morphologies and Application in Solvent-Free Benzyl Alcohol Oxidation. Applied Surface Science 2020, 505, 144473. https://doi.org/10.1016/j.apsusc.2019.144473.
(2) 	Santra, C.; Auroux, A.; Chowdhury, B. Bi Doped CeO2 Oxide Supported Gold Nanoparticle Catalysts for the Aerobic Oxidation of Alcohols. RSC Adv. 2016, 6 (51), 45330–45342. https://doi.org/10.1039/C6RA05216A.
(3) 	Song, H.; Liu, Z.; Wang, Y.; Zhang, N.; Qu, X.; Guo, K.; Xiao, M.; Gai, H. Template-Free Synthesis of Hollow TiO2 Nanospheres Supported Pt for Selective Photocatalytic Oxidation of Benzyl Alcohol to Benzaldehyde. Green Energy & Environment 2019, 4 (3), 278–286. https://doi.org/10.1016/j.gee.2018.09.001.
(4) 	Reddy, V. G.; Jampaiah, D.; Chalkidis, A.; Sabri, Y. M.; Mayes, E. L. H.; Bhargava, S. K. Highly Dispersed Cobalt Oxide Nanoparticles on Manganese Oxide Nanotubes for Aerobic Oxidation of Benzyl Alcohol. Catalysis Communications 2019, 130, 105763. https://doi.org/10.1016/j.catcom.2019.105763.
(5) 	Schünemann, S.; van Gastel, M.; Tüysüz, H. A CsPbBr3/TiO2 Composite for Visible-Light-Driven Photocatalytic Benzyl Alcohol Oxidation. ChemSusChem 2018, 11 (13), 2057–2061. https://doi.org/10.1002/cssc.201800679.
(6) 	Kobayashi, H.; Higashimoto, S. DFT Study on the Reaction Mechanisms behind the Catalytic Oxidation of Benzyl Alcohol into Benzaldehyde by O2 over Anatase TiO2 Surfaces with Hydroxyl Groups: Role of Visible-Light Irradiation. Applied Catalysis B: Environmental 2015, 170–171, 135–143. https://doi.org/10.1016/j.apcatb.2015.01.035.
(7) 	Tamiolakis, I.; Lykakis, I. N.; Armatas, G. S. Mesoporous CdS-Sensitized TiO2 Nanoparticle Assemblies with Enhanced Photocatalytic Properties: Selective Aerobic Oxidation of Benzyl Alcohols. Catalysis Today 2015, 250, 180–186. https://doi.org/10.1016/j.cattod.2014.03.047.
(8) 	Khawaji, M.; Chadwick, D. Au–Pd NPs Immobilised on Nanostructured Ceria and Titania: Impact of Support Morphology on the Catalytic Activity for Selective Oxidation. Catalysis Science & Technology 2018, 8 (10), 2529–2539. https://doi.org/10.1039/C7CY02329D.
(9) 	Keshri, K. S.; Spezzati, G.; Ruidas, S.; Hensen, E. J. M.; Chowdhury, B. Role of Bismuth on Aerobic Benzyl Alcohol Oxidation over Ceria Polymorph-Supported Gold Nanoparticles. Catalysis Communications 2020, 140, 106004. https://doi.org/10.1016/j.catcom.2020.106004.
(10) 	Mandal, S.; Santra, C.; Bando, K. K.; James, O. O.; Maity, S.; Mehta, D.; Chowdhury, B. Aerobic Oxidation of Benzyl Alcohol over Mesoporous Mn-Doped Ceria Supported Au Nanoparticle Catalyst. Journal of Molecular Catalysis A: Chemical 2013, 378, 47–56. https://doi.org/10.1016/j.molcata.2013.05.011.
(11) 	Zheng, H.; Wei, Z.-H.; Hu, X.-Q.; Xu, J.; Xue, B. Atmospheric Selective Oxidation of Benzyl Alcohol Catalyzed by Pd Nanoparticles Supported on CeO2 with Various Morphologies. ChemistrySelect 2019, 4 (19), 5470–5475. https://doi.org/10.1002/slct.201900757.
(12) 	Li, B.; Zhang, B.; Nie, S.; Shao, L.; Hu, L. Optimization of Plasmon-Induced Photocatalysis in Electrospun Au/CeO2 Hybrid Nanofibers for Selective Oxidation of Benzyl Alcohol. Journal of Catalysis 2017, 348, 256–264. https://doi.org/10.1016/j.jcat.2016.12.025.
(13) 	Lei, L.; Liu, H.; Wu, Z.; Qin, Z.; Wang, G.; Ma, J.; Luo, L.; Fan, W.; Wang, J. Aerobic Oxidation of Alcohols over Isolated Single Au Atoms Supported on CeO2 Nanorods: Catalysis of Interfacial [O–Ov–Ce–O–Au] Sites. ACS Appl. Nano Mater. 2019, 2 (8), 5214–5223. https://doi.org/10.1021/acsanm.9b01091.
(14) 	Hu, Z.; Zhou, G.; Xu, L.; Yang, J.; Zhang, B.; Xiang, X. Preparation of Ternary Pd/CeO2-Nitrogen Doped Graphene Composites as Recyclable Catalysts for Solvent-Free Aerobic Oxidation of Benzyl Alcohol. Applied Surface Science 2019, 471, 852–861. https://doi.org/10.1016/j.apsusc.2018.12.067.
(15) 	Fu, X.; Feng, J.; Wang, H.; Ng, K. M. Room Temperature Synthesis of a Novel $\upgamma$-MnO2hollow Structure for Aerobic Oxidation of Benzyl Alcohol. Nanotechnology 2009, 20 (37), 375601. https://doi.org/10.1088/0957-4484/20/37/375601.
(16) 	Hu, Z.; Zhao, Y.; Liu, J.; Wang, J.; Zhang, B.; Xiang, X. Ultrafine MnO2 Nanoparticles Decorated on Graphene Oxide as a Highly Efficient and Recyclable Catalyst for Aerobic Oxidation of Benzyl Alcohol. Journal of Colloid and Interface Science 2016, 483, 26–33. https://doi.org/10.1016/j.jcis.2016.08.010.
(17) 	Alhumaimess, M.; Lin, Z.; He, Q.; Lu, L.; Dimitratos, N.; Dummer, N. F.; Conte, M.; Taylor, S. H.; Bartley, J. K.; Kiely, C. J.; Hutchings, G. J. Oxidation of Benzyl Alcohol and Carbon Monoxide Using Gold Nanoparticles Supported on MnO2 Nanowire Microspheres. Chemistry – A European Journal 2014, 20 (6), 1701–1710. https://doi.org/10.1002/chem.201303355.
(18) 	Santra, C.; Pramanik, M.; Bando, K. K.; Maity, S.; Chowdhury, B. Gold Nanoparticles on Mesoporous Cerium-Tin Mixed Oxide for Aerobic Oxidation of Benzyl Alcohol. Journal of Molecular Catalysis A: Chemical 2016, 418–419, 41–53. https://doi.org/10.1016/j.molcata.2016.03.026.
(19) 	Olmos, C. M.; Chinchilla, L. E.; Villa, A.; Delgado, J. J.; Hungría, A. B.; Blanco, G.; Prati, L.; Calvino, J. J.; Chen, X. Size, Nanostructure, and Composition Dependence of Bimetallic Au–Pd Supported on Ceria–Zirconia Mixed Oxide Catalysts for Selective Oxidation of Benzyl Alcohol. Journal of Catalysis 2019, 375, 44–55. https://doi.org/10.1016/j.jcat.2019.05.002.
(20) 	Ji, H.; Ebitani, K.; Mizugaki, T.; Kaneda, K. Oxidation of Benzyl Alcohol Aiming at a Greener Reaction. Reaction Kinetics and Catalysis Letters 2003, 78 (1), 73–80. https://doi.org/10.1023/A:1022509815590.
(21) 	Günay, M. E.; Yildirim, R. Neural Network Analysis of Selective CO Oxidation over Copper-Based Catalysts for Knowledge Extraction from Published Data in the Literature. Ind. Eng. Chem. Res. 2011, 50 (22), 12488–12500. https://doi.org/10.1021/ie2013955.


