FROM python:3.8

RUN pip install mlflow azure-storage-blob numpy scipy pandas scikit-learn cloudpickle boto3

COPY train.py .
COPY wine-quality.csv .

ENTRYPOINT ["python", "train.py", "--alpha", "0.5", "--l1-ratio", "0.5"]