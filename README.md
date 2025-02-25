# LocalLLM
Instructions on how to set up and run your own LLM.

## Author
[Noah Pursell](https://github.com/noahapursell)
[noahapursell@gmail.com](mailto:noahapursell@gmail.com)

## Running your own LLM

### Step 1: Download Ollama

[Ollama](https://ollama.com/) is a tool that allows you to download and run Large Language Models (LLMs) on your computer. 

1. Download Ollama from the Ollama website. Make sure you choose the right version for your OS.
  ![image](https://github.com/user-attachments/assets/e268bc9d-ac8d-4751-8d2c-a5af3a8310da)
2. Run the downloaded executable.
  ![image](https://github.com/user-attachments/assets/345480c3-84fd-4ef6-adfb-9f40a9b0d43b)
3. Verify installation by opening a new terminal on your computer, and running `ollama`. If Ollama is installed correctly, you will see something like this:
  ![image](https://github.com/user-attachments/assets/78ae1c81-429d-48ca-a1e2-d374ee004ebf)

### Step 2: Download a LLM

After downloading Ollama, you can now download an LLM. There are many different ones to choose from. Larger LLMs will generally perform better but require more computing to run. If you are running on a laptop without a dedicated GPU, I recommend using a model with less than 3 billion parameters. 

1. View [Ollama's LLM Library](https://ollama.com/library).
2. Choose an LLM. In this tutorial, we will use *deepseek-r1*, *1.5b*. This means we are using a 1.5 billion parameter deepseek model.
3. Copy the LLM model reference. In this case, it is `deepseek-r1:1.5b`
  ![image](https://github.com/user-attachments/assets/d58a4e58-1964-462e-aeec-f81c5df52579)
4. Go to a new terminal on your computer.
5. Run `ollama pull <model reference>`. In my case, I ran `ollama pull deepseek-r1:1.5b`. This will download the model.
  ![image](https://github.com/user-attachments/assets/b2b6d2e9-afe0-4173-a9c9-79e7dcce1f17)
6. Upon a successful download, you will see a *success* message.
  ![image](https://github.com/user-attachments/assets/ddc4ebb0-c628-40f3-acab-e97761861b16)

### Step 3: Run the LLM

After downloading the model, you can now run it. Running the model will allow you to chat with the model. For now, will will run it in the terminal. Later, we will show you how to interact with a model in a pretty ChatGPT-like UI.

1. In a terminal, run `ollama run <model reference>`. In my case, I ran `ollama run deepseek-r1:1.5b`.
2. This will prompt me for a message to start the conversation
  ![image](https://github.com/user-attachments/assets/e1e21e6e-f15d-47e0-873b-f5e8e6c09bd3)
3. You can now chat with the LLM.
  ![image](https://github.com/user-attachments/assets/f13d914c-223b-4808-8988-dfd57fb431e2)

## Using a Nice UI

Now that we can talk with our LLM, it would be nice to not have to use the terminal. One tool we can use is [Open WebUI](https://openwebui.com/) - a tool that gives us a ChatGPT-like interface for our local LLM. 

### Step 1: Install OpenWebUI

There are several ways to install OpenWebUI, including Docker, pip, Kustomize, and Helm. In this tutorial, we will install OpenWebUI using pip.

To install OpenWebUI with pip, we must first create a new Python environment (venv). Ensure you have Python 3 installed. Instructions to create and activate a Python environment vary between Windows and macOS. Follow the appropriate instructions below for your operating system.

**Windows**

1. Open Command Prompt.
2. Navigate to your project directory and run: `python -m venv openwebui-env`.
3. Activate the virtual environment: `openwebui-env\Scripts\activate`.

**macOS**

1. Open terminal.
2. Navigate to your project directory and run: `python3 -m venv openwebui-env`.
3. Activate the virtual environment: `source openwebui-env/bin/activate`.

After activating your virtual environment, we can now install OpenWebUI using pip.
1. Run `pip install open-webui`.
2. Run `open-webui serve`.
3. Wait for the startup process to complete.
  ![image](https://github.com/user-attachments/assets/04283b3a-0741-4494-b6a6-d0ee36cc5f31)
4. On your machine, go to the [local OpenWebUI site](http://localhost:8080/auth)
  ![image](https://github.com/user-attachments/assets/44e1e42d-7184-43fa-b3e5-40a9ca4a3d1e)
5. Click "Get Started"
6. Create an account.
  ![image](https://github.com/user-attachments/assets/5319febb-e29b-49cd-93ea-b84082cd003e)
7. Chat with your model!
  ![image](https://github.com/user-attachments/assets/7a4df0be-52e6-4ae0-addf-be79e53f71f7)

## Closing Remarks

In this demo, we have used Ollama to download an run our own LLM, and used OpenWebUI to interact with with a functional UI. 

Going forward, feel free to explore different model types and different OpenWebUI functionalities (like tools). Additionally, learn how to connect your code to your local LLM with tools like LangChain.






