### Selezionare tutti gli uffici, ordinati per nazione

```SQL
SELECT *
FROM office_db.offices
ORDER BY country;
```

### Selezionare tutti gli uffici, ordinati per nazione e per città

```SQL
SELECT *
FROM office_db.offices
ORDER BY country && city;
```

### Selezionare tutti gli impiegati, ordinati per titolo e per nome

```SQL
SELECT *
FROM office_db.employees
ORDER BY title,name ASC;
```
### Contare quanti impiegati condividono lo stesso ufficio

```SQL
SELECT office_id, COUNT(id) AS employee_count
FROM office_db.employees
GROUP BY office_id;
```

### Contare quanti impiegati condividono la stessa estensione

```SQL 
SELECT extension,COUNT(id) as employee_count 
FROM office_db.employees
GROUP BY extension
```

### Selezionare tutti i prodotti con quantità inferiore a 500 pezzi

```SQL 
SELECT * 
FROM office_db.products
WHERE qty < 500;
```

### Selezionare tutti i prodotti Ford

```SQL 
SELECT * 
FROM office_db.products
WHERE name LIKE '%FORD%';
```

### Contare quanti prodotti Ford hanno quantità inferiore a 500 pezzi

```SQL
SELECT * 
FROM office_db.products
WHERE name LIKE '%FORD%' && qty < 500;
```