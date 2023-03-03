## issues_37
```sql
create table "Departments" (
    id serial,
    department_name varchar(200)        not null
);
create table "Staff" (
    id serial,
    first_name     varchar(100)        not null,
    last_name      varchar(100)        not null,
    username       varchar(100) unique not null,
    phone          varchar(15)  unique not null,
    is_active      boolean default true,
    region_id      integer,
    salary         integer
);
create table "Teachers" (
    id serial,
    first_name     varchar(100)        not null,
    last_name      varchar(100)        not null,
    username       varchar(100) unique not null,
    phone          varchar(15)  unique not null,
    subject        varchar(30)         not null,
    is_active      boolean default true,
    region_id      integer,
    group_id       integer
);
create table "Students" (
    id             serial,
    first_name     varchar(100)        not null,
    last_name      varchar(100)        not null,
    username       varchar(100) unique not null,
    phone          varchar(15)  unique not null,
    department_id  integer             not null,
    dob            date,
    date_joined    date,
    date_graduated date,
    is_graduated   boolean default false,
    is_active      boolean default true,
    gpa            real    default 0,
    grade          integer             not null,
    region_id      integer,
    group_id       integer
);
create table "Groups" (
    id serial,
    group_name     varchar(100)        not null,
    subject        varchar(30)         not null,
    teacher_id     integer
);
create table "Regions" (
    id serial,
    region_name    varchar(200)        not null
);
create table "Subjects"(
    id serial,
    subject_name varchar(100),
    subject_id integer
 )
 ```
 
 ![image](https://user-images.githubusercontent.com/122611882/222671409-1edfbbbf-c23a-435b-9082-f649c88e5f66.png)

![image](https://user-images.githubusercontent.com/122611882/222697779-cc49f85c-2bbf-4216-ac5b-ec0a62fa6356.png)

![image](https://user-images.githubusercontent.com/122611882/222697846-b2860140-5ece-4b59-9d47-99aa60b664b6.png)

![image](https://user-images.githubusercontent.com/122611882/222697899-32305841-723c-4eb7-b126-4e9781732cdd.png)

![image](https://user-images.githubusercontent.com/122611882/222697940-6cd282b4-4465-48ad-aac5-9b35982ed007.png)

![image](https://user-images.githubusercontent.com/122611882/222698000-443cd440-d999-48f3-afcc-9a6ba10053fa.png)
