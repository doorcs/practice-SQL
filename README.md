``` SQL
SELECT D.dname AS Department, AVG(E.salary) AS average_salary
FROM EMP E
JOIN DEPT D ON E.dno = D.dno -- SQL에는 할당문이 없기 때문에 `==` 대신 `=` 사용
WHERE E.position = 'Manager' -- string literal에는 single quote 사용
GROUP BY D.dname
HAVING AVG(E.salary) > 7000
ORDER BY average_salary DESC
LIMIT 3;
```
> FROM (&& JOIN) -> WHERE -> GROUP BY -> HAVING -> SELECT -> ORDER BY -> LIMIT ; ( 실행 순서 )

- - -

- 24.09.20 SQLD 합격
