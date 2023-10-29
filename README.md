# NaturalLanguageProcessingWithTransformers
Natural Language Processing with Transformers by Lewis Tunstall, Leandro von Werra &amp; Thomas Wolf.

Sunday, January 15, 2023

docker run --gpus all -it -v $(realpath ~/):/tf/All -v /home/rob/Data2:/home/rob/Data2 --env HF_DATASETS_CACHE=/home/rob/Data2/huggingface/datasets --env TRANSFORMERS_CACHE=/home/rob/Data2/huggingface/transformers -p 8888:8888 -p 6006:6006 hfptl:20221222

01_Introduction.ipynb
Run Date: Sunday, January 15, 2023
Run Time: 00:00:29

02_classification.ipynb
Run Date: Sunday, January 15, 2023
Run Time: 00:04:38

03_transformer-anatomy.ipynb
Run Date: Sunday, January 15, 2023
Run Time: 00:00:10

04_multilingual-ner.ipynb
Having out of memory issues with this notebook. Numerous installs to this image ...
So saved the file, exited docker, want to restart the container ... so ...

(base) rob@KAUWITB:~$ docker container ps -a
CONTAINER ID   IMAGE            COMMAND                  CREATED             STATUS                     PORTS     NAMES
c135df6d6af8   hfptl:20221222   "/opt/nvidia/nvidia_…"   About an hour ago   Exited (0) 2 minutes ago             determined_wing

docker container start determined_wing
docker container logs determined_wing

Sigh ... nope ... continues to run out of memory, even with a reduced batch size. 

05_text-generation.ipynb
Nope! Runs out of GPU ram ...

06_summarization.ipynb
Nope! Runs out of GPU ram ...

### Saturday, October 28, 2023

Trying 05_textgeneration.ipynb again in the newest huggingface transformers docker image which is running inside the container hfpt_Oct28.

Hmm interesting ... it now runs! With the 2070 Super! Nice!

Gonna also try the 06_summarization.ipynb again ... 

I had to run 'pip install py7zr'

1:49PM Wow ... so I renamed Data2/HuggingFace to Data2/HuggingFace_ then reran this notebook ... AND IT STILL RUNS! So where I thought the models were being saved to is wrong! ... Are they being saved into the container??

