# DB University Day 3

## GROUP BY querys


## 1. Contare quanti iscritti ci sono stati ogni anno

```
SELECT COUNT(*) AS `enrolments`, YEAR(`enrolment_date`) AS `enrolment_year`
FROM `students`
GROUP BY `enrolment_year`;
```

## 2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio

```
SELECT COUNT(*) AS `teachers_quantity`, `office_address`
FROM `teachers`
GROUP BY `office_address`;
```

## 3. Calcolare la media dei voti di ogni appello d'esame

```
SELECT AVG(`vote`) AS `average_vote`, `exam_id` 
FROM `exam_student`
GROUP BY `exam_id`;
```

## 4. Contare quanti corsi di laurea ci sono per ogni dipartimento

```
SELECT COUNT(*) AS `degrees_quantity`, `department_id`
FROM `degrees`
GROUP BY `department_id`;
```