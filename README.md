# Santander-Risk-Analysis

This project was a team effort undertaken under the guidance as a MBSA capstone project, at the suggestion of Ryan Morrissey, Director, Business Control & Risk Management, Consumer & Business Banking at Santander Bank, N.A.

The purpose of the project was to create an automated, adaptable and scaleable risk assesment program to track key risk indicators (KRIs), action driver (AD) status and Priority Rating in Issue Management.

A dataset of Santander Risk Programs was used. The first step was to clean the set: remove or impute null values, modify data types and restructure the data. Python was used for it’s extensive library toolset which includes Pandas and scipy.

After the data was cleaned, AHP (analytic hierarchy process) weights were calculated in Excel spreadhseets, in order to mathemtically compare the importance of risk alerts. A scale for relative concern of decision-making parameters was defined, and then a pairwise comparison matrix was created. Next, the matrix was normalized and its consistency was calculated, in order to determine whether the usability of the obtained weights. The weights were subsequently combined to mathemtically determine a rank that contains the essence of all the underlying decision-making criteria in the form of numbers.

For KRIs (key risk indicators), if a value stays on amber or red for too long, it can drag the whole business line down. In order to mathemitcally quantify this phenomenon, a weight was applied to the indicators who remained on an amber/red alert for consecutive months.

The weights were scaled to a range between 0-100 using a min max scaler. The end result was a Tableau Dashboard that allows for quick, intuitive and interactive visualizations of the various risk alerts. Users have the ability to filter for specific dates, alerts, or business areas.

Once the weights were obtained, a business area average was computed, which is a vital piece of the puzzle to analyze overall area performance. Moreover, a benchmark for performance assesment was calculated in the form of percentiles.

The image below illustrates the aforementioned steps, which were meticulously and sequentially executed in order to attain the desired results.





This repository contains all of the files used in this project, including the original dataset, the Python Jupyter Notebook used for data processing, the Excel spreadsheet used to calculate the AHP weights, the Tableau Dashboards, as well as the final document further detailing the project. A requirements.txt file is included, which can be used to install the libraries required to run the Python code using:

pip install requirements.txt  or
pip3 install requirements.txt

The designed model has the potential to streamline risk tracking, enhance problem-solving time and benefit intelligent prioritization. It is scaleable because even if more rating criteria are added in the future, the AHP implementation ensures that the resulting numeric output will remain rational and consistent, thereby aptly capturing the sentiment of the ratings.

An interesting extension would be quantifying the effect of one risk program on another. Domain expertise can be leveraged in combination with this model in order to maximize risk tracking efficiency.
