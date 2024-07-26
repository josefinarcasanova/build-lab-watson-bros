[![](https://img.shields.io/badge/IBM%20Cloud-powered-blue.svg)](https://cloud.ibm.com)

# IBM Build Lab | Watson Brothers

- [IBM Build Lab | Watson Brothers](#ibm-build-lab--watson-brothers)
  - [1. Introduction](#1-introduction)
    - [1.1. About Watson Brothers](#11-about-watson-brothers)
    - [1.2. Business Challenge](#12-business-challenge)
  - [2. About Challenge](#2-about-challenge)
    - [2.1. Goal](#21-goal)
    - [2.2. Repository Structure](#22-repository-structure)
  - [3. Implementation Considerations](#3-implementation-considerations)
    - [3.1. General considerations](#31-general-considerations)
    - [3.2. Environment considerations](#32-environment-considerations)
  - [4. Solution Delivery](#4-solution-delivery)
    - [4.1. Deliverables](#41-deliverables)
    - [4.2. Focal Points](#42-focal-points)
  - [References](#references)
  - [Authors](#authors)

## 1. Introduction

### 1.1. About Watson Brothers

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/64/Warner_Bros_logo.svg/1965px-Warner_Bros_logo.svg.png" width="20%"/>
</p>


Watson Brothers Entertainment Inc. (commonly known as Watson Bros. or abbreviated as WB) is an American film and entertainment studio headquartered at the Watson Bros. Studios complex in Armonk, New York. Founded in 1911 by two brothers, Thomas Jr. and Arthur Watson, the company established itself as a leader in the American film industry before diversifying into animation, television, and video games, and is one of the largest companies in the world.

They are pioneers in the usage of technology, and actively advocate for its usage to improve their customer's experience.

### 1.2. Business Challenge

Watson Bros. wishes to better understand how their customers feel about the movies they go see in their cinemas. They have attempted to achieve this several times, with little success, due mainly to technological difficulty, high costs, and data privacy concerns. Now that Generative AI is being massively adopted, and knowing IBM's watsonx is the most trusted platform for Enterprise AI, they want to try again.

Watson Bros. has requested IBM to develop a solution able to classify movie reviews as either "Positive" or "Negative", based solely on the review itself. To develop this solution, Watson Bros. is willing to provide access to a database containing a wide list of movie reviews.

## 2. About Challenge

### 2.1. Goal

You must engineer a prompt using one of the [supported foundation models available with watsonx.ai](https://dataplatform.cloud.ibm.com/docs/content/wsj/analyze-data/fm-models.html?context=wx) to classify the [movie reviews](assets/data/movie-reviews-train.csv) given to you so that if a new review is inputted, the system will respond either `Positive`, `Negative` or `Unknown` if it's impossible to determine.

Additionally, to prove your solution's performance, you must evaluate its results (based on the [test dataset](assets/data/movie-reviews-test.csv)) on the following metrics:
- Accuracy
- Precision & Recall
- F1-Score

To do this, you have been given a train/test dataset in `csv` format containing three columns: `row number`, `review` and `score`, where score is `1` for Positive reviews and `0` for Negative ones. In addition, a [Jupyter notebook sample](/notebook/notebook.ipynb) has been provided to you, which you must improve so it meets the criteria mentioned above.

### 2.2. Repository Structure

```
.
├── assets/           # Repository Assets
│   ├── images/       # Images used in the present document
│   └── data/         # Train & Test datasets
├── notebook/         # Application source code
└── README.md         # Present document
```

## 3. Implementation Considerations

- Solution must be developed on the Jupyter Notebook present in this repository.
- Documentation **must be** in English.
- In order to meet the client's industry's Safety Quality and Compliance requirements, it is **imperative** for this solutions to meet the [best development standards](https://owasp.org/www-project-secure-coding-practices-quick-reference-guide/stable-en/02-checklist/05-checklist) and practices for security and scalability.
- Access credentials to all services required for solution development will be provided to you by The Client via e-mail.

When developing your solution:

- Be sure to comment your code.
- Add markdown cells for explaining graphics, evaluation results, or any information that isn't self-explanatory.
- Do not share your access credentials with others.

### 3.1. General considerations

You will be using Generative AI for this challenge. These models drive high costs and must be used carefully. Platform usage will be monitored throughout the challenge. 

Non-challenge use of the platform is strictly **prohibited** and will result in challenge **disqualification**.

### 3.2. Environment considerations

It is recommended you run this Jupyter notebook locally. You can do this via [Visual Studio Code](https://code.visualstudio.com/docs/datascience/jupyter-notebooks).

Create your local environment (one time only):

```
cd notebook/
python -m venv .venv
```

> **Note:** if you get a `command not found: python`, try with `python3`.

Activate your environment

```
source .venv/bin/activate
```

Install dependencies (one time only):

```
pip install -r requirements.txt
```

Then, open your Jupyter notebook on Visual Studio Code and use it normally.

## 4. Solution Delivery

After the challenge is presented to you, you will receive an e-mail containing the access credentials you'll need to complete it. You will have **one week** to complete the challenge, starting from the moment the e-mail is sent to you.

### 4.1. Deliverables

Once you have finished the challenge, or your time has ran out, you must deliver the following assets:

1. **Source code**
   1. Resulting Jupyter Notebook in `.zip` format. Remove any credentials before sending. Review [implementation considerations](#3-implementation-considerations) before submission.
   2. Do not fork this repo. Contribute locally instead.
2. **Showcase video**
   1. Video detailing what the challenge was about, how you implemented it, and what you learned from the experience.
   2. Duration must be between **two and five minutes**. This will be taken into consideration during evaluation.
   3. `.mp4` format is preferred.
   4. The video **must be in English**, so the client's Technical Leadership can understand it.

For privacy and security reasons, assets must be *submitted via e-mail attachment*, instead of forking/commiting to this repository.

### 4.2. Focal Points

Communication, both for questions and delivery purposes, must be sent to:

- `Gabriela Retamosa`. Senior Build Lab Leader, SSA & MX. [gabyretamosa@uy.ibm.com](mailto:gabyretamosa@uy.ibm.com)
- `Josefina R. Casanova`. Build Lab Engagement Lead, Americas. [josefinarcasanova@ibm.com](mailto:josefinarcasanova@ibm.com)
- `Sebastian Fripp`. Associate Build Lab Engagement Lead, Americas. [sfripp@ibm.com](mailto:sfripp@ibm.com)
- `Nadia dos Santos`. Associate Build Lab Engagement Lead, Americas. [nadiadossantos@ibm.com](mailto:nadiadossantos@ibm.com)

## References

- [watsonx.ai Python SDK](https://ibm.github.io/watsonx-ai-python-sdk/)
- [watsonx.ai documentation](https://dataplatform.cloud.ibm.com/docs/content/wsj/getting-started/welcome-main.html?context=wx)
- [Tutorial | Create a confusion matrix in Python](https://developer.ibm.com/tutorials/awb-confusion-matrix-python/)

## Authors

- [Josefina R. Casanova](https://github.com/josefinarcasanova) | IBM Build Lab Engagement Lead Americas
