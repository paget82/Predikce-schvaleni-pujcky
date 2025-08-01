# Projekt: Predikce schválení půjčky pomocí různých modelů strojového učení 

## Cil projektu:

Společnost má zájem o automatizaci procesu schvalování půjček na základě informací poskytnutých zákazníky při vyplňování online žádosti. Vývoj modelů strojového učení by měl společnosti umožnit lépe předpovídat schválení půjčky a zároveň urychlit rozhodování o tom, zda žadatel splňuje podmínky pro její získání.

##  Soubory ke stažení:
-  [Jupyter Notebook](predikce%20schvaleni%20pujcky.ipynb) – Predikce schválení půjčky + Postup
-  [CSV](loan.csv) – Dataset


## Zadání:
*   Analyzovat zákaznická data poskytnutá v datové sadě (EDA)
*   Vytvořit různé modely strojového učení, které dokážou předpovědět schválení půjčky



**Modely strojového učení použité v tomto projektu:** 
1. Logistic Regression
2. K-Nearest Neighbour (KNN)
3. Support Vector Machine (SVM)
4. Naive Bayes
5. Decision Tree
6. Random Forest
7. Gradient Boost


## Popis datové sady:
Tato datová sada obsahuje 13 proměnných:
* 8 kategoriálních proměnných,
* 4 spojité proměnné a
* 1 proměnnou pro identifikátor půjčky (Loan ID).



### Data: 
* 614 záznamů
* Loan_ID – Referenční číslo půjčky (unikátní ID)
* Gender – Pohlaví žadatele (Muž nebo Žena)
* Married – Rodinný stav žadatele (ženatý/vdaná nebo svobodný/á)
* Dependents – Počet členů rodiny
* Education – Vzdělání/kvalifikace žadatele (vysokoškolské nebo nižší)
* Self_Employed – Zaměstnanecký status žadatele (ano – OSVČ, ne – zaměstnaný/jiný)
* ApplicantIncome – Měsíční příjem žadatele
* CoapplicantIncome – Měsíční příjem spolužadatele
* LoanAmount – Požadovaná částka půjčky
* Loan_Amount_Term – Doba splatnosti půjčky (v dnech)
* Credit_History – Záznam o předchozí úvěrové historii (0: špatná, 1: dobrá)
* Property_Area – Umístění nemovitosti (venkov / příměstská / městská oblast)
* Loan_Status – Stav žádosti o půjčku (Y: schváleno, N: zamítnuto)

### Výsledek:
Obecně lze říci, že všechny modely mohou dosáhnout až 70% přesnosti.
Nejvyšší dosažená přesnost je 81 %.
