# Dockerfile-backend
FROM python:3.8-slim
WORKDIR /app
COPY requirements-backend.txt ./
RUN pip install --no-cache-dir -r requirements-backend.txt
# Download NLTK data
RUN python -m nltk.downloader vader_lexicon punkt stopwords wordnet
COPY . .
ENV FLASK_APP=app.py
CMD ["flask", "run", "--host=0.0.0.0", "--port=5000"]