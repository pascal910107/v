# create virtual environment
<!-- virtualenv venv -->
<!-- virtualenv --python=C:\Users\User\AppData\Local\Programs\Python\Python38\python.exe myenv -->
python -m venv venv

# enter virtual environent
.\venv\Scripts\activate

# download library
pip install -r requirements.txt
pip install --upgrade numpy
pip install --upgrade --force-reinstall numba
pip install --upgrade Cython
pip install --upgrade pyzmq

# build monotonic align
cd monotonic_align/
mkdir monotonic_align
python setup.py build_ext --inplace
cd ..

# run
python VC_inference.py --model_dir ./OUTPUT_MODEL/G_latest.pth --share True

python VC_inference.py --model_dir ./OUTPUT_MODEL/G_4000.pth --share True