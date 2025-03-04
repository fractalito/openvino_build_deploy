FROM python:3.10-slim
ARG HF_TOKEN
ENV HF_TOKEN=${HF_TOKEN}


# Install the required packages
COPY ./requirements.txt .
RUN python -m pip install --upgrade pip
RUN pip install --no-cache-dir -r requirements.txt

# Copy the requirements file into the container
WORKDIR /app
COPY . .

# Command to run the application
CMD ["python", "main.py", "--hf_token", "${HF_TOKEN}"]
