# QuestionSolver
- Python code that solves a multiple choice question with 3 answer choices. It requires access to Google Console. 
- I loved working on this project. It is cool how you can write code to answer a question for you and I will keep trying to improve it

Things to improve on:
  - Take in any number of answer choices
  - Take any kind of photo with question and answer choice in it and be able to extract useful information from it
  - Acquire better search results(could be done applying diffrent boolean operators in the search) 
  - Come up with better analysis methods(chop off common suffixes on certain answer choices, see how close an answer choice is to something    in the question, use some advanced NLP methods, make a datatable with previously answered questions and apply ML techniques)

Update:
  - Added apostrophe remover and plurality remover for better accuracy 
  
Requirements:
  - Python compiler(I am using Jupyter Notebook)
  - For Google Vision API:
    1. You will need to create a service account key
    2. https://cloud.google.com/vision/docs/reference/libraries (useful link)
  - For Google Custom Search Engine API:
    1. You  will need to create a custom search engine, obtain custom engine ID and API Key
    2. https://developers.google.com/custom-search/json-api/v1/overview (useful link)

How it works:
  1. Give it a picture of the question with 3 choices
  2. Using the Google Vision API, it will detect all the text in picture. The API returns a JSON file
  3. JSON files get converted into python list and important parts of the data are extracted
  4. Then, using the Google Custom Search Engine API, it will search the web
  5. All the search results get compiled into a pandas Dataframe
  6. Then, the dataframe is anaylzed to count the frequency of the answer choices 
  7. Frequency for each choice is displayed
 
*USE AT OWN RISK, IT IS NOT PREFECT!!
