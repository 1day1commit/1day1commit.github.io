---
layout: post
title: '[MySQL] DML'

categories:
  - Database

tags:
  - [Database]

toc: true

permalink: /:title/

date: 2021-12-15T10:28:11+0900
lastmod: 2021-12-15T10:28:11+0900
---

<br>
<br>

DML은 Data Manipulation Language의 약자로 데이터를 조작하는 쿼리문들을 뜻합니다. `INSERT, UPDATE, DELETE` 문이 대표적인 쿼리문 입니다. `INSERT`는 데이터를 테이블에 넣는 것을 의미하고, `UPDATE`는 이미 테이블에 들어간 데이터를 수정하고, `DELETE`는 데이터를 테이블에서 삭제합니다.

<br>

# INSERT INTO (table)

```
INSERT INTO artists (name) VALUES ('폴킴');
INSERT INTO artists (name) VALUES ('이무진');
INSERT INTO artists (name) VALUES ('스탠딩에그');
```

```
SELECT * FROM artists;
```

<img width="623" alt="2021-12-15_13-59-14" src="https://user-images.githubusercontent.com/87692499/146126167-532eef16-2082-4a35-80d2-d2a8d9a0751f.png">

<br>

# UPDATE (table) SET (column)

이미 테이블에 들어간 데이터를 수정하려면 `UPDATE`를 사용하면 됩니다.

```
UPDATE artists SET name='이무진' WHERE id=2
```

```
SELECT * FROM artists;
```

<img width="631" alt="2021-12-15_16-00-39" src="https://user-images.githubusercontent.com/87692499/146138944-16bd860c-8aab-4e7d-89ed-4576aefb37f1.png">

`이무진`이 `리무진`으로 수정되었습니다.

<br>

# DELETE FROM (table)

```
DELETE FROM artists WHERE name='리무진';

SELECT * FROM artistis;
```

<img width="614" alt="2021-12-15_16-05-24" src="https://user-images.githubusercontent.com/87692499/146139496-26ad0a6c-de7f-4e87-bb7e-a86d13f1811d.png">

<br>

# 정리

- DML은 Data Manipulation Language의 약자로 데이터를 조작하는 쿼리문들을 뜻합니다.
- 테이블에 데이터를 넣을 때 사용하는 명령어는 `INSERT INTO {table_name} (column1, column2, ... ) VALUES (data1-1, data1-2, ... ), (data2-1, data2-2, ... );`의 형태로 사용합니다.
- 이미 입력된 데이터를 수정하는 명령어는 `UPDATE {table_name} SET {column_name}={new_data} WHERE {condition};`입니다.
- 기존에 입력되어 있던 데이터를 지우는 명령어는 `DELETE FROM {table_name} WHERE {condition};`입니다.
