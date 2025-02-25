# GradeGuard
GradeGuard is an AI bot that evaluates the usage of ai in the completion of a project, exam, test, assignment, or class exercise by students and grade them according. <br>
It is robust system that promote academic integrity by detecting AI-generated content in student assignments.

![image](https://github.com/user-attachments/assets/80637cdd-6a07-4fb7-a597-38576109de77)

<br><br>
<hr/>

# Run Project Locally 
*It is advisable you use two terminal to run*
## Backend
cd to back-end
```bash
cd back-end
```

### Install packages
```bash
pip install -r requirements.txt
```

In the `back-end` directory, create a `.env` file using your editor or terminal

```bash
touch .env
```

Open the env file and paste the following 

```js
OPENAI_API_KEY=
ASSISTANT_ID=
API_TOKEN=
```

For Admin or Product owner Only
- Create the assistant
```bash
python ./src/create_model.py
```
- copy the `ASSISTANT_ID` output in the terminal and paste i you `.env` file
![image](https://github.com/user-attachments/assets/fa931b77-5c95-4853-87c8-60d4fe4d448e)




### Update the `.env`
Ask Admin or Product owner for the api keys
- Update the env `OPENAI_API_KEY` with your [open api key](https://help.openai.com/en/articles/4936850-where-do-i-find-my-openai-api-key) 
- Update the env `ASSISTANT_ID` with your [assistant id](https://platform.openai.com/docs/api-reference/assistants/object)
- Update the env `API_TOKEN` with any random string of any length


## Start Back-end Server
```bash
python ./src/app.py
```
![image](https://github.com/user-attachments/assets/8af63509-73d2-488d-86df-3d8b9df4e87e)


<br><br><br><br><br><br><br>
## Frontend
cd to frontend

```bash
cd front-end
```

Install dependecies
```bash
npm install
```


In the `front-end` directory, create a `.env` file using your editor or terminal

```bash
touch .env
```

Open the env file and paste the following 

```js
VITE_API_TOKEN=
VITE_API_URL=http://127.0.0.1:5000
```

### Update the `.env`
Your `VITE_API_TOKEN` value must be the same value as `API_TOKEN` in your `back-end/.env` file


## To run Frontend
```bash
npm run dev
```
<img src='./front-end/src/assets/FrontEnd Server.png'>



# Technology
 Using OpenAI Assistant, we trained GTP 4o
 ## Training data
 - `back-end/src/training_data/training.json` contains the evaluation data
 - `back-end/src/training_data/fallback.json` contains the fallback data to handle non ai-related question

## Frontend
- React
- Fetch API
- HTML 5
- CSS 3

## Backend
- Python
- Flask
- OpenAI

# Limitation
- Hallucination
- Inconsistent/Invalid Json return
- Not good at handling multiple scenrio. 
