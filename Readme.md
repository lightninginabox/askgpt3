<h1 align="center">Ask Me Anything GPT-3</h1>

<div align="cetner">
  <p align="center">A simple wrapper for OpenAI GPT-3 question/answer engine.</p>
  <img src="assets/website.png" alt="AMA GTP3"></img>
</div>

<br>

## 💫 Demo
Here is a free and publicly available instance that you can play with

**https://amagpt3.com**

<br>

## 🔌 Installation

### API
```
$ make setup-api
```

### Website
```
$ make setup-website
```

### Cli
```
$ make setup-cli
```

### Slack Bot
```
$ make setup-slack
```

<br>

## Configuration
You need to provide your own OPENAI API key (Required)
```
$ export OPENAI_API_KEY=<YOUR KEY HERE>
```
You can get one by signing up for free here 👉 https://openai.com/api/

```
$ export OPENAI_MODEL=<MODEL>
```
By default, `curie` model  is used.

More infos here 👉 https://beta.openai.com/docs/api-reference/answers

<br>

For Slack bot, you need to provide the following tokens:
```
$ export SLACK_APP_TOKEN=xoxb-xxx
$ export SLACK_BOT_TOKEN=xapp-xxx
```
More infos here 👉 https://api.slack.com/bot-users

<br>

## 🚀 Usage
### API
```
$ make run-api
[2022-01-27 15:44:56 +0100] [1560229] [INFO] Running on http://127.0.0.1:8000 (CTRL + C to quit)
```

```
$ http POST :8000/ask question="Your question here"
```

Example:
```
$ http POST :8000/ask question="how cool is elon musk ?"
HTTP/1.1 200
content-length: 28
content-type: application/json
date: Thu, 27 Jan 2022 14:47:19 GMT
server: hypercorn-h11

{
    "answer": "He is a genius."
}
```


### Website
```
$ make run-website
[2022-01-27 15:48:57 +0100] [1564095] [INFO] Running on http://127.0.0.1:8000 (CTRL + C to quit)
```
Then open the url http://127.0.0.1:8000 in your browser

Screenshot:

<div align="cetner">
  <img src="assets/website.png" alt="AMA GTP3"></img>
</div>


### Cli
```
$ source .venv/bin/activate
$ ./cli.py ask "YOUR QUESTION HERE"
```

### Slack
```
$ make run-slack
```

<br>

## ⚒️  Built using
- [Quart](https://github.com/pallets/quart)
- [HTTPX](https://github.com/encode/httpx/)
- [Click](https://github.com/pallets/click/))

<br>

## 🔧 Testing
```
$ make dev
```

```
$ make test
```

<br>

## ✍️  Author

Badr BADRI @pythops

<br>

## ⚖️  License
AGPLv3

Copyright © 2022 Badr BADRI @pythops

<br>

## ℹ️  OpenAI Policies
Anyone who is willing to copy this  code and launch their own Q&A app, must follow OpenAI going live policy 👉 https://beta.openai.com/docs/going-live
