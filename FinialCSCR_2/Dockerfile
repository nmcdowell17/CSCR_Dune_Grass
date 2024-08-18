FROM python:3.10-slim-buster
WORKDIR /app
COPY requirements.txt requirements.txt 
RUN pip install --no-cache-dir -r requirements.txt 
COPY . .
RUN pip install jupyter  
EXPOSE 8888 
CMD ["jupyter", "notebook", "--ip", "0.0.0.0", "--allow-root"]