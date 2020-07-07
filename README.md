## **Task :**
The goal of this project is to create a small app in python, An application that processes the two data files [students.csv , teachers.parquet]. The application should use both files to output a report in json listing each student and the teacher.
The application will be used with both local and files stored in aws S3, so there should be an easy way to specify the location of these files and the output json.

 

## **System requirements :**
- OpenSSL 1.1.1
- python 3.5

 

## **Modules used :**
- botocore : for accessing S3 bucket files and exception handling corresponding to S3 functionalities
- pandas : for processing csv and parquet files
- os : to access files from local directory
- json : to output a proper json formatted data
- pyarrow : to access parquet files 
 

## **Set up environment :**
> - **Create an environment :**
> ```python
> python -m virtualenv task_env
> ```
> 
>  
> - **Activate environment :**
> ```python
> source task_env/bin/activate
> ```
> 
>  
> - **Install requirements**
> ```python
> pip install requirements.txt
> ```


## Environment variable setting :
> - If file is in local :
> ```bash
> export FILE_LOCATION=<location of folder where files are located>
> ```

> - If file is in S3 :
> ```bash
> export FILE_LOCATION=s3://bucketname
> ```
 

## **Commands to run :**
- **Git clone** :
```git
git clone <url>
```

- **Command to run :**
```python
python3 -m venv /path/to/task_env        # could be any path
source /path/to/task_env/bin/activate
pip install -r requirements.txt
python3 src/readfile-app.py
```


- **Docker commands :**
```dockerfile
$ docker build -t my-python-app .
$ docker run -it --rm --name my-running-app my-python-app
```