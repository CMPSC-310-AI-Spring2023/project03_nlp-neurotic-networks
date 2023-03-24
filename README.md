# Project 3: Climate and Natural Language Processing

## Deadlines:

- _Part 1 Script Planning (Topic Selection)_: March 27th by 9:50am
- _Part 2 Project Progress_: March 29th by 4:20pm
- _Part 1 Completed Script_: April 3rd by 9:00am
- _Part 1 and 2 Project Demonstration_: April 5th, 2:30pm - 4:20pm
- _Part 2 Final Code and Report_: April 7th by 9:00am

## Table of Contents

- [Summary](#summary)
- [Objectives](#objectives)
- [Code of Conduct](#code-of-conduct)
- [Learning](#learning)
- [Assignment Specification](#assignment-specification)

  - [PART 1: AI & Climate Change](#part-1:-ai-&-climate-change)
  - [PART 2: Text Generation for Synopsis](#part-2:-text-generation-for-synopsis)

- [Project Progress](#project-progress)

- [Project Demonstration](#project-demonstration)

- [Required Deliverables](#required-deliverables)

- [Assignment Assessment](#assignment-assessment)

- [GatorGrade](#gatorgrade)

- [Receiving Assistance](receiving-assistance)

## Summary

This project assignment invites you to work individually or in a team or two (or three) to explore association of climate change and AI, and implement a learning agent that generates text related to climate to highlight this important civic challenge. You are also responsible for writing a detailed report, stored in the file `writing/report.md`. This is a Markdown file that must adhere to the standards described in the [Markdown Syntax Guide](https://guides.github.com/features/mastering-markdown/).

## Objectives

To learn how AI both contributes to and can be used to provide some solutions to climate change problems. To learn to use a `tensorflow` and other similar software libraries and a neural network algorithm for the natural language processing tasks. To gain understanding of natural language processing techniques that can be used for text generation. To evaluate the performance of the machine learning algorithm used for the natural language processing tasks. To reflect on the design and development of the algorithm and to highlight ethical issues raised in the generated text.

## Code of Conduct

Throughout the completion of this project you must adhere to the [community guidelines](https://github.com/CMPSC-310-AI-Spring2023/course_information/blob/main/community_guidelines.md) that we developed as a class. In addition to reporting any violations of the code of conduct using [this form](https://forms.gle/W6Kf2jt1DmmKEdAs6), please make sure that you attest to the fact that you followed the code of conduct. Students who think that the class should revise some aspect of the guidelines must use the GitHub issue tracker for that repository to suggest, discuss, and implement any required changes.

## Learning

To review material on neural networks please read section 4.1.from the [Dive into Deep Learning](https://d2l.ai/chapter_multilayer-perceptrons/mlp.html) book and section 7.5 from the [Artificial Intelligence: Foundations of Computational Agents](https://artint.info/2e/html/ArtInt2e.Ch1.html) textbook. To learn about `tensorflow` and its use you may follow [tensorflow tutorials](https://www.tensorflow.org/tutorials). To see how to use Google's colab environment to run Tensorflow applications, please refer to [its documentation](https://colab.research.google.com/notebooks/intro.ipynb).

If you have not done so already, please read all of the relevant [GitHub Guides](https://guides.github.com/) that explain how to use many of the features that GitHub provides.

## Assignment Specification

Climate change refers to broad range of changes in temperatures and weather patterns (ref:[UN: What is Climate Change](https://www.un.org/en/climatechange/what-is-climate-change), [NASA: Climate](https://climate.nasa.gov/)). Human actions, for example burning of fossil fuels, have been main contributors to this change since 1800s, and this global climate change is already impacting water resources, food supply, our health, our infrastructure, and ecosystem (ref: [NOAA: climate change impacts](https://www.noaa.gov/education/resource-collections/climate/climate-change-impacts)).

AI has been identified as an important partner in tackling climate change issues, from reducing greenhouse gas emissions to helping humans adjust to climate change (ref:[Tackling climate change with AI](https://www.climatechange.ai/)). However, AI also has a negative carbon footprint, especially in NLP, where best models such as GPT have a big carbon footprint and are environmentally unfriendly [Green AI](https://cacm.acm.org/magazines/2020/12/248800-green-ai/fulltext?mobile=false).

In this project, students are invited to investigate impact of AI on climate change, and then use neural network based algorithm with `tensorflow` or a similar library to create an agent that is able to generate text to bring attention to climate challenge that humanity faces. The specific text to be generated is a synopsis for a movie or show about climate that may help us think through different possibilities of (future) impacts of climate change. Then, you will analyze your generated text, the carbon footprint of your production of this generated text, and reflect on ethical issues surrounding AI and climate.

### PART 1: AI & Climate Change

First, you need to investigate relationship between AI and climate change, both from a negative and a positive side. Using this information, we will develop a simple slideshow/video about AI and climate change. Each team/individual will select one specific topic to explore and contribute both information and visual aids for their selected topic. Topics can include but are not limited to:

- Green AI: how AI can be more environmentally friendly and sustainable
- Red AI: carbon footprint of AI models
- Various AI aids to contribute to fighting climate change (for example, use satelite and IoT data for planning and decision making, enhance management of smart grids, optimize supply chain, etc.)

Once you have selected a topic to explore, you must complete the [AI & CLIMATE SCRIPT](https://docs.google.com/document/d/1x3yEEixeV2GbIjCItC6k5BlX9f4Lpmop0tXnuBq8JgI/edit?usp=sharing) by filling in one of the Act boxes in the Google form above. The topic selection must be completed by class time on Monday, March 27th. Your team's full script must be completed by class time on Monday, April 3rd.

### PART 2: Text Generation for Synopsis

In the second part of the project, to further highlight climate crisis, you will generate a synopsis (one paragraph) for a hypothetical movie or show about climate change.

#### 2.1\. Data Gathering

To generate relevant text you first need relevant data. There are many TV shows or movies that might provide text that wold be useful for your task. Movies such as "Don't Look Up" and "The Day After Tomorrow" are good examples as they contain storylines involving the climate change that seems feasible (or at least represents a foreseeable straight line from our current situation) and takes it a step further. This allows the viewers to ask important questions about future implications of climate change. There are also many popular and scientific articles about climate change and its impact. You should feel free to experiment with providing your algorithm with various textual data, some possibly completely unrelated to the subject of climate change.

**Your first task is to gather useful textual data.** For example, you can get the subtitle (.str) files from websites such as [subscene](https://subscene.com) or [opensubtitles](https://www.opensubtitles.org/en/search/subs), where each file contains the transcript of an episode/movie, or you can search for synopsis data on [kaggle](https://www.kaggle.com). There are also tools (for example, written in Python) that can parse through and download subtitle data automatically. You may need to do some pre-processing to get a dialog of each episode without extraneous text and/or convert file types (from `srt`, for example, to a program-readable format). Tools such as [pysrt](https://github.com/byroot/pysrt) and many others can be helpful in the pre-processing tasks.

#### 2.2\. Text Generation using Tensorflow

**Once you have the relevant data, you are to use `tensorflow` and/or another similar library, and a machine learning algorithm of your choice that is based on the idea of neural networks to automatically generate synopsis (few sentences or one paragraph) for a show or movie about climate.** You must write Python code for this task (giving ChatGPT a prompt and getting its result in the web interface is not sufficient). While your generated text does not need to be structurally or grammatically correct, it should produce some phrases that can be used to extract meaning of what a show or a movie about the climate might be about. You should run experiments to evaluate and improve your implementation.

There are many examples and tutorials for generating text using `tensorflow`. For example, there is a [tensorflow guide on text generation](https://www.tensorflow.org/text/tutorials/text_generation) and [guide on using lstm for text generation](https://www.kaggle.com/code/shivamb/beginners-guide-to-text-generation-using-lstms). There are also some existing projects that provide tools to automatically generate text. For example, [textgenrnn project](https://github.com/minimaxir/textgenrnn) uses recurrent neural network and allow you to train the model on new text relatively easily (see basic example code in the repository). More recent AI-based text-generation model, called GPT, which is trained on huge amounts of text all around the internet, simplifies text generation process for the developer. Older version of GPT have Python integration, such as [gpt-2 simple](https://github.com/minimaxir/gpt-2-simple), which is a Python package which provides many functionalities for model management and generation control, allowing you to easily fine tune GPT-2 on your text.

You will need to either install `tensorflow` locally or via Docker, please refer to the [official website](https://www.tensorflow.org/install) for instructions for both. Alternatively, you can run `tensorflow` applications directly in a browser using Google's Colaboratory platform. Since training and testing natural language models is computationally expensive, with big models running for hours or days on a regular CPU machine, use of GPU is encouraged. Google's Colaboratory platform allows you to execute programs using `tensorflow` on GPU for free. Go to [colab's website](https:// colab.research.google.com), click on "File", "New notebook". Now you can write the code and run it in the web browser. You can also download the program either as a notebook (.ipynb file) or as a Python program (.py file) by going to "File", "Download".

In this step, keep an eye on the time it takes to run your learning algorithm. You will reflect on your carbon footprint in the report.

#### 2.3\. Supplemental Production

Finally, to "sell" your script's synopsis, you are to produce a supplemental production in the form of a movie/show poster. The automatically generated script is likely not to sufficiently represent or look like a script. If this is the case, you should manually modify your script before creating a poster. You can create a poster yourself or have AI tool, such as [DALLE](https://labs.openai.com/) or [Night Cafe](https://nightcafe.studio/) create one that fits the description of your script.

## Project Progress

By the lab time on Wednesday, March 29th, you should have done significant research on the selected topic for Part 1, and you should at least obtain your data, and investigate and select machine learning implementation. TL and the instructor will check in with each team and complete progress evaluation to ensure you are on target for project completion.

## Project Demonstration

During the lab session on Wednesday, April 5th, each team will be given an opportunity to demonstrate their project in the lobby of the campus center. The demonstration will comprise of "pitching" the synopsis they automatically generated, aided by their "movie/show poster". The class and possibly outside members will participate in an interactive demonstration session, where everyone will be able to view each pitch and generated synopsis.

## Required Deliverables

This assignment invites you to submit the following deliverables.

1. Script topic selection in the [Script Google Doc](https://docs.google.com/document/d/1x3yEEixeV2GbIjCItC6k5BlX9f4Lpmop0tXnuBq8JgI/edit?usp=sharing) due on March 27th by 9:50am.\
2. Participation in project progress check in during the lab on March 29th.
3. Completed script for the video/slideshow on AI & Climate submitted in the [Script Google Doc](https://docs.google.com/document/d/1x3yEEixeV2GbIjCItC6k5BlX9f4Lpmop0tXnuBq8JgI/edit?usp=sharing) due on April 3rd by 9:00am.
4. A properly completed and commented source program(s). Please make sure your source code is located inside "src" directory in your project03 repository.
5. A production artifact to supplement your automatically generated synopsis in the form of a poster.
6. The completed report, stored in `/writing/report.md` and written in Markdown, that provides answers in all remaining sections (follow the prompts inside the report document).
7. Participation in project demonstration during the lab on April 7th.

All class sessions March 24th--27th will be used for project work. Lab session on March 29th will be used for project work as well.

## Assignment Assessment

The grade that a student receives on this assignment will have the following components.

- **GitHub Actions CI Build Status [up to 5%]:**: For project03 repository associated with this assignment students will receive a checkmark grade if their last before-the-deadline build passes. This is only checking some baseline writing and commit requirements. An additional reduction will given if the commit log shows a cluster of commits at the end clearly used just to pass this requirement. An addition reduction will also be given if there is no commit during lab work times. All other requirements are evaluated manually.

- **Engagement in Script Making [up to 20%]:**: A portion of the grade is based on the quality of engagement and work produced for the AI & Climate video/slideshow production.

- **Mastery of Verbal Explanation during Progress Check In and Demonstration [up to 15%]:**: Since the timely project development and the ability to communicate technical details of a project is crucial to building successful software applications, a portion of students' lab grade will be determined based on the participation in progress check in (5%) and the quality of the project demonstration (10%). Also, since sparking interest in climate change challenge is crucial to our ability to address this challenge, a part of this grade will be based on the creativity of your supplemental production and its ability to enhance the attractiveness of your synopsis.

- **Mastery of Technical Writing [up to 10%]:**: Students will also receive a checkmark grade when the responses to the writing questions presented in the `report.md` reveal a proficiency of both writing skills and technical knowledge. To receive a checkmark grade, the submitted writing should have correct spelling, grammar, and punctuation in addition to following the rules of Markdown and providing conceptually and technically accurate answers.

- **Mastery of Technical Knowledge and Skills [up to 50%]**: Students will receive the largest portion of their assignment grade when their project implementation reveals that they have mastered all of the technical knowledge and skills developed during the completion of this project. As a part of this grade, the instructor will assess aspects of the project including, but not limited to, the completeness and the correctness of the program(s), the appropriate use of libraries and neural network algorithm, and the use of effective source code comments and Git commit messages.

All grades for this project will be reported through a student's gradebook GitHub repository.

## GatorGrade

You can check the baseline requirements of this project by running department's assignment checking `gatorgrade` tool. To use `gatorgrade`, you first need to make sure you have Python installed. If not, please see:

- [Setting Up Python on Windows](https://realpython.com/lessons/python-windows-setup/)
- [Python 3 Installation and Setup Guide](https://realpython.com/installing-python/)
- [How to Install Python 3 and Set Up a Local Programming Environment on Windows 10](https://www.digitalocean.com/community/tutorials/how-to-install-python-3-and-set-up-a-local-programming-environment-on-windows-10)

Then, you need to install `gatorgrade`:

- First, [install `pipx`](https://pypa.github.io/pipx/installation/)
- Then, install `gatorgrade` with `pipx install gatorgrade`

Finally, you can run `gatorgrade`:

`gatorgrade --config config/gatorgrade.yml`

## Receiving Assistance

If you are having trouble completing any part of this project, then please talk with either the course instructor during the lab session. Alternatively, you may ask questions in the Slack workspace for this course. Finally, you can schedule a meeting during the course instructor's office hours.
