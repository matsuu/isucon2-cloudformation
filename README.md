# AWS CloudFormation templates for isucon2

- http://blog.livedoor.jp/techblog/archives/67726489.html
- https://github.com/tagomoris/isucon2

# How to use

- Sign in to the [AWS Management Console](https://console.aws.amazon.com/console/home).
- Access to EC2.
- Select Key Pairs.
- Push "Create Key Pair" button or note down your "Key Pair Name".
- Access to CloudFormation.
- Push Create New Stack button.
- Choose "Upload a Template File" and upload the template following.
- Set your "Key Pair Name" to KeyName.
- Status goes CREATE\_COMPLETE and check Outputs tab.

# Templates 

## isucon2-standalone.template

```
 :5001     :80
   |        |
+--+--------+---------------+
|                           |
| test - reverse - app - db |
|         proxy             |
+---------------------------+
```


## isucon2-rev-app2-db.template

```

                 +-----+
     +---------+ + app + +----+
 :80 |         |/+-----+\|    |
-----+ reverse *         * db |
     |  proxy  |\+-----+/|    |
     +---------+ + app + +----+
                 +-----+
```

## isucon2-test.template

```
 :5001
   |
+--+---+
|      |
| test |
|      |
+------+
```


## isucon2-test-revappdb.template

```
 :5001
   |
+--+---+      +--------------------+
|      |  :80 |                    |
| test +------+ reverse - app - db |
|      |      |  proxy             |
+------+      +--------------------+
```

## isucon2-test-rev-app2-db.template

```
 :5001
   |                      +-----+
+--+---+      +---------+ + app + +----+
|      |  :80 |         |/+-----+\|    |
| test +------+ reverse *         * db |
|      |      |  proxy  |\+-----+/|    |
+------+      +---------+ + app + +----+
                          +-----+
```

## isucon2-test-rev-app2-rds.template

```
 :5001
   |                      +-----+
+--+---+      +---------+ + app + +-----+
|      |  :80 |         |/+-----+\|     |
| test +------+ reverse *         * rds |
|      |      |  proxy  |\+-----+/|     |
+------+      +---------+ + app + +-----+
                          +-----+
```
