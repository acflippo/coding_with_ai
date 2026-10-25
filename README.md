# Introduction

This is a learning session on how to use AI to aid in coding in python. This is targeted to people who is comfortable installing and debugging new software onto your laptop and has a beginner's experience in coding preferrably in python.

## Pre-requisites:

The instructions provided here have been tested on MacOS and if you are running Windows or Linux, you should be comfortable to translate the instructions for your own OS. Other requirements include:

1. Github account to clone this repo to your local machine.
2. A virtual python environment on your local machine such as venv, conda, Anaconda.  See [Install_Python.md](Install_Python.md)
3. Install Cursor Desktop App from https://cursor.com/, get a Cursor account (e.g. free tier or Cursor Plus ~$8/month).

# Provide AI guidelines

If you're using an IDE (integrated development environment) such as Claude or Cursor for the first time or using VSCode with Claude or another AI coding system, it's __VITAL__ to provide some guidelines or instructions for the AI to follow.

We will go over this in class on how to provide the AI with the following minimum guidelines:

- If you change any code, let me review it before making the change
- Tell the agent the runtime virtual environment to use.  In our case, we will use a python virtual environment
- Tell the agent your preferences in directory names such as
    - put all source codes in a directory called src
    - put all output such as csv or image files in the result directory
- Use this guideline https://best.openssf.org/Secure-Coding-Guide-for-Python/ for best practices in secure coding 

If your main usage is coding, you can find some pre-define skills in the marketplace (more on this later).  Ask the AI to save your instructions as global preferences.  For Claude, it will save it as CLAUDE.md.  For Cursor, it will save it as a SKILL.md.  You can edit these files manually if you like.

We will be using a free tier of Cursor and work within the limits of our token allowance.  If you run out of tokens before you finish the lab, it's ok. You can either wait until your token allowance reset or upgrade to the next paid tier for 1 month to finish the lab.  As of 10/30/2026, Cursor Plus is $8/month.

# How to provide AI instructions

Give AI specific, succinct and short instructions.  It's less effective to tell AI what-not-to-do, it seems to confuse it  so provide positive actions for the AI agent (e.g. what you want it to do). 

Personally, I do my thinking in pseudo code by talking out loud.  I've done this for years so it came naturally for me to use AI to develop sections of the code.  This contains the amount of thinking AI needs to do and to focus on a task.

AI doesn't seem to have a good naming convention for variables so if you have a preference, provide it. It also does not know when to use global versus local variables. Beware how the generated variables and objects interact inside your code, so you should review the code before running or checking it into a repo, amongst many other caveats when using generated AI code. 

<p align="center">👉 The Buck Stops with You 👈</p>

## Exercise: Chart Stock Price 

Our hands-on exercise is to write some code to download stock prices and chart it.  Here are the over arching goals of our exercise:

1. Find a stock you want to graph the stock price for the past 10 years. Choose a specific ticker symbol such as AAPL, MSFT, NVDA or a stock of your choice.  Check out https://www.tradingview.com/screener/

2. Ask the agent to write the code for the function download_stock_price()

3. Write code for the function graph_stock_price()

4. Develop the main function to using the functions available.

5. We will be using a notebook format (e.g. Jupyter notebook) so we can run each section ourselves to see what the AI is doing.

6. Optional: If time allows, create a python file instead of a notebook to graph stock price by passing an argument.

__Note__: 
- If you run into an error, you can ask AI to look into the error. 
- You can also provide a screenshot of the issue into the chat window and ask the agent to debug it.
- If you don't know where it is saving some skills or rules, you can ask it.
- AI agent can debug itself if you run into an agent issue.
- When you edit a file but forgot the save it onto disk, the agent won't see what you've changed.  Make sure you always save your changes.
- If you update the runtime environment such as installing a new package installation, you must reload it before it will take effect.  The AI can't see what you're doing in another terminal window.