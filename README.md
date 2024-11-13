Step 0: Download Project and Dataset Files
Download Project File: Access the project file on Google Drive,(https://drive.google.com/drive/folders/1uSCU4SmC1Li2Tny8kLBeD1wP9IYYHBAp?usp=sharing) download it, and extract it to your preferred directory.
Download Dataset: Visit the dataset page on Kaggle and download the dataset as archive.zip. Extract the contents of archive.zip.

Step 1: Set Up Virtual Environment
Open your command prompt or terminal, navigate to your project folder, and follow these steps:

cmd
Copy code
python -m venv myvenv
This will create a virtual environment named myvenv in the project directory.

Step 2: Activate the Virtual Environment
Activate the virtual environment:

On Windows:

cmd
Copy code
.\myvenv\Scripts\activate
On macOS/Linux:

bash
Copy code
source myvenv/bin/activate
Step 3: Install Project Requirements
Install the necessary libraries listed in requirements.txt:

cmd
Copy code
pip install -r requirements.txt
Step 4: Organize the Dataset
Rename the extracted dataset folder (e.g., archive) to datasets.

Move data.yaml from the datasets folder to the main project directory.

Update the contents of data.yaml to specify the paths for train, validation, and test data:

yaml
Copy code
train: ./train/images
val: ./valid/images
test: ./test/images

nc: 5
names: ["bicycle", "bus", "car", "motorbike", "person"]
Remove the original data.yaml file from within the datasets folder to avoid confusion.

Your project folder structure should now look like this:

cmd
Copy code
.
├── datasets
│   ├── test
│   │   ├── images
│   │   └── labels
│   ├── train
│   │   ├── images
│   │   └── labels
│   └── valid
│       ├── images
│       └── labels
├── data.yaml
├── object-detection-prediction-yolov8.ipynb
├── object-detection-using-yolov8.ipynb
├── readme.md
└── requirements.txt
Step 5: Running the Jupyter Notebooks
Open object-detection-prediction-yolov8.ipynb in Visual Studio Code (VS Code).

In the notebook, locate the kernel selection button at the top right and choose myvenv as the kernel.

Execute the cells in the notebook sequentially.

Note: In the Visualizing Results section, the paths to images might need to be updated. Check the runs folder created during model training for images and other files, then adjust the paths in the notebook accordingly.
Open object-detection-using-yolov8.ipynb and add links to the dataset (train, test, and valid).

Step 6: Specify Paths for Videos and Images
In object-detection-prediction-yolov8.ipynb, provide the path to your video file where it’s needed in the code.
In the simulation file, update the paths to the images folder to match your folder structure.
After completing these steps, you should be ready to run the project and view results for traffic signal optimization using computer vision. Let me know if you run into any issues along the way

Step-by-Step Guide for traffic-simulation.py
Open traffic-simulation.py:

Open the file in your text editor (like VS Code).
Locate the Files:

Make sure untitled_design1.jpg and mod_int.png are in a folder accessible from your project directory. For instance, you might place them in the assets folder along with the other images.
Update the Paths in traffic-simulation.py:

Open traffic-simulation.py in your text editor.
Locate where any additional background or intersection images are loaded, and add paths for untitled_design1.jpg and mod_int.png as needed.
Assign Paths:

Assign paths to the variables for untitled_design1.jpg and mod_int.png according to your folder structure. Here’s an example of how to add these paths:
python
Copy code
# Example paths (update according to your folder structure)
up_signal_image = "./assets/up_signal.png"
down_signal_image = "./assets/down_signal.png"
left_signal_image = "./assets/left_signal.png"
right_signal_image = "./assets/right_signal.png"

car_image = "./assets/car.png"
bus_image = "./assets/bus.png"

mod_int_image = "./assets/mod_int_edited.png"
intersection_image = "./assets/intersection.jpg"

# New image paths
untitled_design_image = "./assets/untitled_design1.jpg"
mod_int_original_image = "./assets/mod_int.png"
Use the Images in the Code:

Ensure that untitled_design1.jpg and mod_int.png are actually referenced in the code. If they’re intended for specific visualization purposes (e.g., background, layout), you might use them similar to other images. Example:
python
Copy code
# Example usage of the images
background = Image.open(untitled_design_image)
layout = Image.open(mod_int_original_image)
Run the Simulation:

After you’ve saved traffic-simulation.py with the updated paths, activate your virtual environment if it’s not already active, and run the script:

cmd
Copy code
python traffic-simulation.py
This should incorporate untitled_design1.jpg and mod_int.png into your traffic simulation. Let me know if there are any specific uses or further customization needed for these images!


![Screenshot 2024-11-07 000347](https://github.com/user-attachments/assets/f27b835b-eb47-4027-b042-baede6a8022e)

![Screenshot 2024-11-07 000347](https://github.com/user-attachments/assets/19ce4afd-9a1e-474f-9598-237bcd7f2520)

![WhatsApp Image 2024-10-25 at 11 14 09_09a285eb](https://github.com/user-attachments/assets/4f6437a1-2b6e-4db2-b497-e07fc1b1bf1e)







