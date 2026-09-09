Para contagem de linhas:
```sql 
SELECT COUNT(*) FROM produtos;
```

Para realizar contagem e nomear a tabela:
```sql
SELECT COUNT(*) AS total_registros 
FROM produtos;
```

Para aplicar filtros nas consultas:

```sql
SELECT COUNT(*) AS produtos_baixo_estoque
FROM produtos 
WHERE estoque >= 10;
```

Para exibir o maior valor:
```sql
SELECT MAX(preco) AS maior_preco
FROM produtos;
```

Caso, você fique curioso e queira saber o nome do prouto mais caro:
```sql
SELECT nome,preco FROM produtos
ORDER BY preco DESC;
```

Para obter a média de uma coluna:
```sql
SELECT AVG(preco) AS media_preços
FROM produtos;
``` 

Para limitar casas decimais:
```sql
SELECT ROUND(AVG(preco),2) AS media_correta 
FROM produtos;
```

Para exibir tudo em uma consulta:
```sql
SELECT 
MAX(preco) AS maior_preco,
MIN(preco) AS menor_preco,
ROUND(AVG(preco),2) AS media  
FROM produtos;
```

Tudo em uma única consulta:
```sql
SELECT 
MAX(preco) AS preço_maior,
MIN(preco) AS preço_menor,
ROUND(AVG(preco),2) AS media,
SUM(estoque) AS total_produtos
FROM produtos;
```

Para somar o total de faturamento, vendendo todos os produtos da Terabyte:
```sql
SELECT SUM(preco * estoque) AS total_faturamento
FROM produtos;
```