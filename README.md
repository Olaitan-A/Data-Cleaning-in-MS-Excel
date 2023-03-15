# Data-Cleaning-in-MS-Excel
A data cleaning project using MS Excel - Transforming a messy dataset from dirty to clean
# Introduction
![FIFA 21 homepge](https://user-images.githubusercontent.com/109909855/225309511-bc13c4d3-6abc-46a8-9e63-6bd4f359ac4d.jpg)
# Introduction
This project was inspired by a data cleaning challenge organized by data professionals on twitter, The dataset provided is a messy FIFA21 dataset gotten  from www.kaggle.com. 
FIFA21 is an association football simulation video game published by Electronic Arts as part of the FIFA series.
# About the dataset
A messy dataset of EA Sports' installment of their hit FIFA series - FIFA21 scraped from www.sofifa.com. The dataset has 18980 rows and 77 columns containing details about each player.
# The Cleaning Process
As stated earlier, my choice of tool for the challenge was microsoft excel.

- After assessing the data to understand what needed to be done in order to take it from messy to clean, A copy of the dataset was made in order to have the original dataset in the event of data loss during cleaning. The dataset was imported into excel through the text import wizard using these steps:
         "Data" tab > "From text/CSV"
         In the "File origin" field, "65001: Unicode (UTF-8)" was selected before loading the data into the excel sheet  
         This step eliminated all special characters earlier noticed in some columns of the dataset during assessment 
         
         
    BEFORE ![Dirty Characters in the data RES](https://user-images.githubusercontent.com/109909855/225361159-e1c31d8a-2de2-441c-8b78-57a2a392ed0a.JPG)  AFTER  ![Neat Characters RES](https://user-images.githubusercontent.com/109909855/225361387-3e85c742-7f9a-4790-bb83-e59be2405ff3.JPG)

- The dataset was checked for duplicate values
 
 ![FIFA NO DUPLICATES FOUND (4)](https://user-images.githubusercontent.com/109909855/225366258-0dce547c-7014-4d9e-a6d5-426b6d5e8c43.JPG)

- The OVA column and POT column - Overall analysis and Potential respectively were formatted to percentages 


    BEFORE ![ovapot- old](https://user-images.githubusercontent.com/109909855/225374175-9fc4e121-8c4f-4475-944d-ff73d82f0e06.JPG)    AFTER   ![image](https://user-images.githubusercontent.com/109909855/225374769-ee17ecff-3297-4d4d-b967-e3f34a19b6b9.png)
 
- The TILDE symbol(~) in the contract column was replaced with a more appropriate symbol, Hyphen (-) using the substitute function SUBSTITUTE syntax


     BEFORE  ![image](https://user-images.githubusercontent.com/109909855/225380270-494726be-b7b9-4234-8812-1ff486b8161b.png)        AFTER    ![image](https://user-images.githubusercontent.com/109909855/225381642-d0352e7a-34c8-4d88-8dc8-ce67101d77c2.png)

- The 'Height' Column had majority of the values in cm while some were in ft and inches, The values in cm were converted to ft and inches using a combination of three functions; TRUNC, ROUND AND MOD  
      The TRUNC function removes the fractional part of the result after dividing the value in cm by 2.54 and 12 (1ft = 12 inches and 1 inch =2.54cm)
      The MOD function returns the remainder after division and the ROUND function rounds the result to a specified number  
    
     Final Formula =TRUNC(cell in cm/2.54/12)&" ' "&ROUND(MOD(cell in cm/2.54,12),0)&" """  
      '&' was used to add the units of ft and inches.
     
     BEFORE   ![image](https://user-images.githubusercontent.com/109909855/225386384-31b022ac-b805-44ca-9673-eb8033096e9e.png)       AFTER    ![image](https://user-images.githubusercontent.com/109909855/225387156-0bce842a-6730-4450-9293-afec3222d031.png)
  

- The columns containing the value,wage and release clause of the players were converted from Euro to Dollars as stated by the dataset dictionary provided. Some values were in thousands(K) while some were in millions(M). The cells containing K were multiplied by 1000 and the cells containing M were multiplied by 1000000 before converting them from euro to dollar.
                                            1 Euro = 1.07 dollar

     BEFORE   ![image](https://user-images.githubusercontent.com/109909855/225389308-824aeceb-8310-4b4d-86a1-3dab2b8f8a52.png)        AFTER    ![image](https://user-images.githubusercontent.com/109909855/225390344-522a0663-90bd-4e47-ae3b-935cab1600b9.png)


- The 'Hits' column had some values with letter 'K' The values were multiplied by 1000 and the resulting column was formatted as number

     BEFORE   ![image](https://user-images.githubusercontent.com/109909855/225391395-eb0627a9-4d39-4f0a-b0b7-4de0ca5cd84b.png)        AFTER    ![image](https://user-images.githubusercontent.com/109909855/225391931-4be9e104-ac9d-4d51-90d6-de946881a42f.png)

