## 1. Contare quanti iscritti ci sono stati ogni anno
```
SELECT 
    COUNT(`id`), YEAR(`enrolment_date`)
FROM
    `students`
    WHERE `enrolment_date`
    GROUP BY YEAR(`enrolment_date`)
```
## 2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio
```
SELECT 
    COUNT(*),`office_address`
FROM
    `teachers`
    WHERE `office_address` IS NOT NULL
    GROUP BY `office_address`
```
## 3. Calcolare la media dei voti di ogni appello d'esame
```
SELECT 
    AVG(`vote`),`exam_id`
FROM
    `exam_student`
    GROUP BY `exam_id`
```
## 4. Contare quanti corsi di laurea ci sono per ogni dipartimento
```
SELECT 
    COUNT(*) AS `total_degrees`, `department_id`
FROM
    `degrees`
    GROUP BY `department_id`
```