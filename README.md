``` SQL
SELECT D.dname AS Department, AVG(E.salary) AS average_salary
FROM EMP E
JOIN DEPT D ON E.dno = D.dno
WHERE E.position = 'Manager' -- string literal에는 single quote 사용
GROUP BY D.dname
HAVING AVG(E.salary) > 7000
ORDER BY average_salary DESC
LIMIT 3;
```

> FROM (&& JOIN) -> WHERE -> GROUP BY -> HAVING -> SELECT -> ORDER BY -> LIMIT ; ( 실행 순서 )
