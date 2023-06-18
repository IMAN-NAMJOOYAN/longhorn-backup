# longhorn-backup
**Using external minio as longhorn baskupstore**

```
1- create a bucket in minio (for example: longhorn)
2- create secretkey and acceeskey for bucket
3- create a folder on bucket (for example: longhorn)
```

![image](https://github.com/IMAN-NAMJOOYAN/longhorn-backup/assets/16554389/e0182201-2bcb-446c-a041-eee8e22c591a)

```
4- on kubernetes cluster create a secret for access to minio server:
- Create base64 secret data:
  echo -n <Your AccessKey> | base64
  echo -n <Your SecretKey> | base64
  echo -n <Your Endpoint> | base64
  # Exapmle for endpoint: echo -n http://192.168.1.8:9000 | base64

```
