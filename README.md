This repository contains a Dockerfile that demonstrates a common error:  assuming the existence of a file (requirements.txt) without proper error handling. The solution demonstrates a robust approach to handle missing dependencies. 

**Bug:** The original Dockerfile attempts to install Python packages using `pip3 install -r requirements.txt`. If `requirements.txt` is missing, the build fails. 

**Solution:** The solution handles missing `requirements.txt` gracefully by checking for its existence before attempting installation.  If missing, it provides an informative message.