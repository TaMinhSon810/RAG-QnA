# RAG-QnA

## Prerequisites

- Python 3.7 or later

## Installation

- Click here to open [Google Colab](https://colab.research.google.com/) notebook and then log into your account
- Open the ```RAG.ipynb``` file and create a copy
- Change the run time of your notebook from CPU to GPU
- Follow the colab file to run the project

## Deploying the Chatbot using Ngrok

**Note**: This project deploys the Chatbot using Ngrok in Colab.

**Ngrok**, similar to localtunnel, is a tool that creates a tunnel between your localhost and the internet. Here are the steps to deploy using Ngrok:
1. Go to [Ngrok](https://ngrok.com/), create an account, and log in.
2. Navigate to the "Your Authtoken" section and copy your authtoken.
3. Return to Colab and run Ngrok with the following commands (in 3. Deploy chatbot using ngrok in `RAG.ipynb`):

```
!ngrok config add-authtoken <your-authtoken>
public_url = ngrok.connect(8000).public_url
print(public_url)
```

## Run the Chainlit app: 
Run the app.py file using the command
```
!chainlit run app.py
```

Wait until app.py completes running (you should see the output "Your app is available at http://localhost:8000" in blue text).<br>Then, open the public_url link to see your result.
