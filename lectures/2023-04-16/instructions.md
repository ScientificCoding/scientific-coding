## Install and run alpaca in a local UI

#### on ubuntu
1. update ubuntu
```
sudo apt update
```
2. install git-lfs (optional, if not pre-installed)
```
sudo apt-get install git-lfs
```
3. clone the UI repo
```
git clone https://github.com/oobabooga/text-generation-webui.git
```
4. download the model
```
git lfs install
git clone https://huggingface.co/chainyo/alpaca-lora-7b
```
5. move the model into respective folder
```
mkdir text-generation-webui/models/chainyo
mv alpaca-lora-7b text-generation-webui/models/chainyo/
```
6. prepare the build
```
cd text-generation-webui
cp .env.example .env
```
Edit .env on line 7 
- use the correct model name `chainyo/alpaca-lora-7b`
- remove the part `--wbits 4` from the line
7. Build and run the docker container
```
docker compose up --build
```
8. Navigate to `<host>:7860/?__theme=dark` to access the UI