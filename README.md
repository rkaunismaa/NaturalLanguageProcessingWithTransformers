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