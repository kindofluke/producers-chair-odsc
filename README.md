# The Producer's Chair ODSC

*Materials for ODSC 2024 Talk: Lights, Camera, AI Action: Building a Movie Pitch by Combining Generative and Predictive AI with DataRobot*

Generative AI is so imaginative and so creative but organizations str4uggle to translate that creativity into real value. By using predictive models along with retrival augemented generation (RAG), we can shape and control how materials are generated. This has real tangible benefits for every day applications: 

1. *Guardrails:* We guard against open ended generation (and hallucinations) by using context and specific prompt templates. 
2. *Explainable AI:* Predictive machine learning can be somewhat opaque. Using AI we can ask an LLM to translate SHAP explanations to the end user and provide more objective guidnace to a future result. 
3. *Tested and Proven*: Take advanatge of rigurous partitioning and testing that is done on predictive AI models to gain confidence in future results. 

# Materials for Today

<img src="TheLastHorizon.png" width="200px"></img>


## Application

Everything we build today comes together at **https://the-producers-chair.glitch.me/** where you can try out AI Generated ideas against the predictive models we build today. *Note that after May 1 the app will go to sleep or when my $25 Anthropic account runs out*. 

If you want to edit the application, you can fork it on Glitch. https://glitch.com/@kindofluke

## Building the Models and Vector DB

There are two notebooks in this repo and also a copy of all the data. In both notebooks keep an eye out for boolean values like this: 

```
## If you want to actually run the data set the following to True
RUN_DATA = False
```
These control certain long-running actions to create the datasets and load them from disk. This is just meant to speed up the process. 

The notebooks do use DataRobot APIs which will require a DataRobot API Key. You can get a free trial at https://www.datarobot.com/trial/ However, there also code cells that build models and the vector DB without DataRobot so a key is not required. 


## System Requirements

1. Python 3.11
2. Install all of the requriements in the requirements.txt file
3. Consider using a cloud hosted notebook such as DataRobot CodeSpaces OR Google Colab becuase the embedding model can be quite large 500mb downloaded to create the vector database. 