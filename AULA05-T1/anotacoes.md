## Update e Delete 
**UPDATE** ou **DELETE** afetam todas as linhas da sua tabela. Logo, **JAMAIS** executar sem o comando `WHERE`.

```mermaid
flowchart LR
A[SELECT com o WHERE] -->B{Retornou a linha certa?}
B--SIM-->C[Update ou DELETE]
B--NÃO-->A
```

![alt text](image.png)


```sql 
UPDATE filmes
SET avaliacao=10
WHERE nome='Tropa de Elite';
```