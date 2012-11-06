# AWS CloudFormation templates for isucon2

http://blog.livedoor.jp/techblog/archives/67726489.html
https://github.com/tagomoris/isucon2

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
   |                       +-----+
+--+---+      +---------+ /+ app +\ +----+
|      |  :80 |         +/ +-----+ \+    |
| test +------+ reverse |           | DB |
|      |      |  proxy  +\ +-----+ /+    |
+------+      +---------+ \+ app +/ +----+
                           +-----+
```

