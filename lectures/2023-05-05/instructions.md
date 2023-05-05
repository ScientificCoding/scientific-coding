## Run image generation models in a local UI

#### on ubuntu
1. update ubuntu
```
sudo apt update
```

2. install git and python environments
```
sudo apt install wget git python3 python3-venv
```

3. install git-lfs (optional, if not pre-installed)
```
sudo apt-get install git-lfs
```

4. clone the UI rep0
```
git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui.git
```

5. launch the UI
```
cd stable-diffusion-webui
python launch.py --listen
```

6. navigate to the UI
```
<your-ip>:7680
```

7. optional: to import models from HuggingFace
```
cd models/Stable-diffusion/
```
example model
```
git lfs install
git clone https://huggingface.co/runwayml/stable-diffusion-v1-5
```
The imported model is now available in the dropdown selection in the UI.