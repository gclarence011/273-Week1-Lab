# Python HTTP Track

Deliverables (Submit to Canvas)  
GitHub repository link
README updates:
## How to run locally:

## Run Service A
```bash
cd service-a
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

## Run Service B (new terminal)
```bash
cd service-b
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

## Test
```bash
curl "http://127.0.0.1:8081/call-echo?msg=hello"
```

Stop Service A and rerun the curl command to observe failure handling.


Success + failure proof (screenshot or pasted output)  
https://github.com/gclarence011/273-Week1-Lab/blob/main/success%2Bfailure%20proof.png

1 short paragraph: “What makes this distributed?”  
Service A and B are communicating over HTTP (over the network) and that they are independent processes. When service A dies, Service B still works, even if it cannot reach Service A. Both services does not share memory as they are separated process and cannot access each other memory. They do not share a clock because the OS gives each processes its own clock. 


