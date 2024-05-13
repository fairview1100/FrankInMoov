<!DOCTYPE html>
<html>
<head>
</head>
<body>

<h1>Coqui TTS install MRL</h1>
<p>Test guide for using Coqui TTS with MyRobotLab</p>

<p>Pre-requisites:</p>
<p>MyRobot Lab installed</p>
<p>Docker or Docker Desktop for Windows installed</p>
<p><p>

Coqui install docs are <a href="https://docs.coqui.ai/en/latest/docker_images.html#start-a-server">Here</a>

<h2>Running Coqui docker image:</h2>

<b>CPU Based:</b>

<p>docker run --rm -it -p 5002:5002 --entrypoint /bin/bash ghcr.io/coqui-ai/tts-cpu</p>
<p>python3 TTS/server/server.py --list_models #To get the list of available models</p>
<p>python3 TTS/server/server.py --model_name tts_models/en/vctk/vits</p>


<b>GPU based:</b>

<p>docker run --rm -it -p 5002:5002 --gpus all --entrypoint /bin/bash ghcr.io/coqui-ai/tts</p>
<p>python3 TTS/server/server.py --list_models #To get the list of available models</p>
<p>python3 TTS/server/server.py --model_name tts_models/en/vctk/vits --use_cuda true</p>


</body>
</html>


