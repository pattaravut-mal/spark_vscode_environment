# Use the official OpenJDK image as the base image
FROM openjdk:11-jre-slim

# Install Python and pip
RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    apt-get clean

# Install PySpark and Google Cloud BigQuery client library
RUN pip3 install    pyspark==3.5.4 \
                    google-cloud-bigquery \
                    bigframes \
                    ipykernel

# Set environment variables for PySpark
RUN PYTHON_VERSION=$(python3 -c "import sys; print(f'{sys.version_info.major}.{sys.version_info.minor}')") && \
    echo "PYTHON_VERSION=$PYTHON_VERSION" && \
    export SPARK_HOME=/usr/local/lib/python${PYTHON_VERSION}/dist-packages/pyspark && \
    export PATH=$SPARK_HOME/bin:$PATH

# Install Node.js version 20
RUN apt-get install -y curl && \
    curl -fsSL https://deb.nodesource.com/setup_20.x | bash - && \
    apt-get install -y nodejs 

# Set the working directory
WORKDIR /workspace
