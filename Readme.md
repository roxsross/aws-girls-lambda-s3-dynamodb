# Gestionando archivos con CSV desde AWS Bucket S3 e insertar en DynamoDB usando Lambda [Python]

Seleccionaremos el archivo CSV "demo.csv" lo subimos a un bucket-s3 creado previamente y procesaremos el archivo y lo enviaremos a la tabla de DynamoDB.

## Arquitectura

![Esta es una imagen](image/arquitecture.png)

## Pasos

### Crear rol para Lambda

- Cree la política que se menciona a continuación. [Policy-Lambda](policy_iam_lambda.json)

### Crear bucket s3 

Hay dos formas para crearlas de forma manual directamente con la consola y automatica usando un script con python pero es importante tener las credenciales de aws

- Con la Consola AWS ir al servicio Bucket s3 - Crear Bucket 

** Opcion Automatizada

- Con el Script en Python [Python-s3](create_s3_bucket.py)

### Crear tabla de DynamoDB

De la misma manera que el s3 se puede realizar desde la consola , con lineas de comando o con scripts

- Con la Consola AWS ir al servicio dynamodb - Crear tabla
Table Name = user
Partition key = id
AttributeType: String
ReadCapacityUnits: 1
WriteCapacityUnits: 1

- Con el Script en Python [Python-dynamodb](create_Dynamodb.py)

### Crear Lambda


## Informacion Complementaria

Comenzando con AWS Boto3 [Medium](https://medium.com/@luiscelismx/comenzando-con-aws-boto3-876fd0d6686f#:~:text=Boto3%20consiste%20en%20un%20conjunto,los%20servicios%20web%20de%20Amazon.).

