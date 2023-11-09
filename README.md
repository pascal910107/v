virtualenv venv
virtualenv --python=C:\Users\User\AppData\Local\Programs\Python\Python38\python.exe myenv
python3.8 -m venv myenv


.\venv\Scripts\activate


pip install -r requirements.txt


python VC_inference.py --model_dir ./OUTPUT_MODEL/G_latest.pth --share True