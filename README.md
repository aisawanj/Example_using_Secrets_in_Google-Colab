
# **Example using Secrets in Google Colab**

Example of connecting database (MySQL) using Secrets in Google Colab

Reference on google colab:  [Click Here](https://colab.research.google.com/github/aisawanj/Example_using_Secrets_in_Google_Colab/blob/main/Example_using_Secrets_in_Google_Colab.ipynb)



## **Key Features**

- Simplify code configuration by securely storing environment variables, file paths, or keys.
- Secret names cannot include spaces.
- Sharing a notebook won’t expose stored secrets (remain confidential)
### Reference using Secrets on Google Colab

![image.png](https://drive.google.com/uc?export=download&id=1b6utQ6MeNXx_XB2oel9cVVRKDlwZ4OnY)



## **Code example**

### Create a variable from the default configuration of Secret names and values on google colab

```bash
from google.colab import userdata
MYSQL_HOST = userdata.get('MYSQL_HOST')
MYSQL_PORT = int(userdata.get('MYSQL_PORT'))
MYSQL_USER = userdata.get('MYSQL_USER')
MYSQL_PASSWORD = userdata.get('MYSQL_PASSWORD')
MYSQL_DB = userdata.get('MYSQL_DB')
MYSQL_CHARSET = userdata.get('MYSQL_CHARSET')

```
### Install pymysql

```bash
!pip install pymysql
import pymysql
```

### Connect to the database

```bash
connection = pymysql.connect(host = MYSQL_HOST,
                             port = MYSQL_PORT,
                             user = MYSQL_USER,
                             password = MYSQL_PASSWORD,
                             db = MYSQL_DB,
                             charset = MYSQL_CHARSET,
                             cursorclass = pymysql.cursors.DictCursor)
```


## **Reference on google colab**

[Click Here](https://colab.research.google.com/github/aisawanj/Example_using_Secrets_in_Google_Colab/blob/main/Example_using_Secrets_in_Google_Colab.ipynb)

## **License**

[MIT](https://choosealicense.com/licenses/mit/)

