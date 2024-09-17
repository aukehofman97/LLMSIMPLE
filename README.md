# LLMxSimple
This is the GitHub Project for a Streamlit application that integrates LLMs to perform data transformations by using FEDeRATED as an intermediate standard.
The code is built up in several layers:

- Main.py is used to run the application in Streamlit. You can run it by inserting streamlit run main.py in the terminal. It calls class in myapp.py.
- Myapp.py contains the code for the streamlit application with the main functionalities. It creates both the layout of the streamlit application and the functionalities. The functionalities are mostly split up in functions that can be found in utils.py.
- Utils.py contains all functions used in the application, such as for getting a response from OpenAI, but also reading and saving files.

Other files:
- The specified Event Types are in the folder EventTypes containing the Golden Standard for data transformation, these will be passed into the prompt.
- The models folder contains Pydantic classes. These classes are used to transform the string format from the OpenAI API into structured JSON format, ensuring correct datatypes and format.
- Prompt.txt contains the main prompt with instructions and constraints for the LLM.
- The learning folder contains all user information that can be used to improve the prompt: uploaded files, selected options, and transformation(s) done by the LLM.
- The UserFeedback folder contains the prompts that are to be used within the 'Further Instructions' option. This might be abandoned in the future, since maybe a LLM is not even necessary for this task.
