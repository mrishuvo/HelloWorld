name: CI/CD Pipeline

on:
  push:
    branches:
      - main
  release:
    types:
      - created

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout code
      uses: actions/checkout@v2

    - name: Set up Docker
      uses: actions/setup-python@v2
      with:
        python-version: 3.8

    - name: Build and push Docker image
      env:
        DOCKER_USERNAME: ${{ secrets.DOCKER_USERNAME }}
        DOCKER_PASSWORD: ${{ secrets.DOCKER_PASSWORD }}
      run: |
        echo $DOCKER_PASSWORD | docker login -u $DOCKER_USERNAME --password-stdin
        docker build -t rafiqulshuvo .
        docker push rafiqulshuvo
