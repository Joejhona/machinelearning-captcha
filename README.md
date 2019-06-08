# Resolviendo CAPTCHA con MACHINELEARNING

### Before you get started

To run these scripts, you need the following installed:

1. Python 3
2. OpenCV 3 w/ Python extensions
 - I highly recommend these OpenCV installation guides: 
   https://www.pyimagesearch.com/opencv-tutorials-resources-guides/ 
3. The python libraries listed in requirements.txt
 - Try running "pip3 install -r requirements.txt"

### Step 1: Extract single letters from CAPTCHA images

Run:

python3 extract_single_letters_from_captchas.py

The results will be stored in the "extracted_letter_images" folder.


### Step 2: Train the neural network to recognize single letters

Run:

python3 train_model.py

This will write out "captcha_model.hdf5" and "model_labels.dat"


### Step 3: Use the model to solve CAPTCHAs!

Run: 

python3 solve_captchas_with_model.py

### Nota

- Se actualizo el script para que corra con la libreria atualizada de OPENCV, archivo extract_single_letters_from_captchas (linea 39) y solve_captchas_with_model (linea 44).
- Sale una advertencia de TensorFlow que indica la pronta depreciación de una herramienta.
- Se modifico los nodos de 32 a 25 y el batch_size de 32 a 25, para que pueda correr, archivo  train_model.py, linea 81 y 88.