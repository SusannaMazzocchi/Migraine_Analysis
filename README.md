# 🏥 Migraine Treatment Efficacy: A Survival Analysis

--------

## 📝 Short introduction on the project
Hi, I'm Susanna! This medical data analysis project focuses on evaluating the efficacy of a treatment based on CGRP monoclonal antibodies over a 36-month period. The overall goal was to analyze a real-world clinical dataset of 179 patients suffering from severe migraines (often refractory to other therapies).

The project was divided into three main parts, done in a team with my classmates. **I was entirely in charge of Task 4: Survival Analysis.** Instead of just predicting *if* a patient would get better, I modeled *when* it would happen, calculating the time needed to achieve at least a 50% reduction in Monthly Migraine Days (MMDs).

--------

## 🛠️ Technologies/tools used
* **Python 3** - The main language for the analysis.
* **Jupyter Notebook** - To write the code and display graphs interactively.
* **Lifelines / Scikit-Survival** - Specific Python libraries for Survival Analysis models.
* **Pandas & NumPy** - For handling and cleaning the clinical dataset.
* **Matplotlib & Seaborn** - To plot the Kaplan-Meier curves and Cumulative Incidence Functions.

--------

## ✨ Features
* **Time-to-Event Modeling:** I turned a classic clinical question into a "time-to-event" problem, defining therapeutic success as the main event.
* **Competing Risk Analysis:** I didn't stop at the basics. I calculated the *Cumulative Incidence Function (CIF)* considering treatment discontinuation as a competing risk against recovery.
* **Clinical Insights:** The model proved there is a 95% probability of therapeutic success for those who stay on the treatment, and that the real results (the drop in migraines) happen very steeply in the first 6-12 months!

--------

## 🚀 Process
For my part (Task 4), I started by defining what the "event" to track was (halving the migraine days). I had to carefully handle *censoring*: patients leaving the study early or reaching the end of the 36 months without hitting the goal yet.
Next, I applied the models to plot the probability curves. When I noticed that some patients stopped the therapy before improving, I introduced a competing risks analysis to make the clinical simulation much more realistic and useful for a real doctor.

--------

## 🧠 What I learned
This task was an amazing discovery! Before this project, I thought "Survival Analysis" was only used to calculate mortality rates. Instead, I learned it's a super powerful tool to predict *any* event over time (like the reaction to a drug). 

I learned how to handle messy medical data, understood the mathematical concept of "censored data" (when you don't have complete info on a patient but can't just throw them out of the dataset), and realized that sometimes a patient's baseline characteristics aren't enough to predict how fast they will respond to a drug. 

--------

## ▶️ How to run the project

1. **Clone the repository:**
   Open your terminal and run:
   ```bash
   git clone [https://github.com/SusannaMazzocchi/Migraine_Analysis.git](https://github.com/SusannaMazzocchi/Migraine_Analysis.git)
   cd Migraine_Analysis

2. Make sure to download the attached datasets (baseline and longitudinal) and place them in the main project folder. The notebook needs both files to load the data correctly.
3. Open the Notebook:
Launch Jupyter to view the whole project (or GooggleColab):

   ```bash
   jupyter notebook mMigraine_Analysis.ipynb
---------

Read the attached Medical application.pdf file to get all the context on the patients and discover the detailed conclusions drawn.
