
## MongoDb - Handson 1

#data - https://prepbytes-misc-images.s3.ap-south-1.amazonaws.com/assets/1640781204638-employee.json


## Task

### 1 .  Create a database , give it name like ""Human_Resource"". Create a collection inside this named ""employee""

```bash
  || use Human_Resource

  || db.employee.insertMany(data)
```

### 2. Query the collection ""employee"" and list all the documents

 ```bash
  || db.employee.find()
```

### 3. Query the collection ""employee"" and list the employees who are having salary more than 30000

```bash
db.employee.find({"salary": {$gt:"30000"}})
```

### 4. Query the collection ""employee"" and list the employees who are having experience more than 2 years.

 ```bash
  || db.employee.find({"overallExp":{$gt:"2"}})
```


### 5. Query the collection ""employee"" and list the employees who are graduated after 2015 and having experience more than 1 year

 ```bash
  db.employee.find({"yearGrad":{$gt:"2015"}, "overallExp":{$gt:"1"}})
```

### 6. Query the collection ""employee"" and update the salary of the employee whose salary is greater than 70000 to 65000

 ```bash
  db.employee.updateOne({"salary":{$gt:"70000"}},{$set:{"salary":"65000"}})
```
### 7. Delete all the documents from ""employee"" where last company is Y"

```bash 
db.employee.deleteMany({"lastCompany":"Y"})
```




    