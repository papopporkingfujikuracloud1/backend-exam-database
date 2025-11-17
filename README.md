# Githup download dataset https://github.com/neondatabase-labs/postgres-sample-dbs

# Setup database

set PGPASSWORD=[My password]

psql -h localhost -p 5432 -U postgres

DROP DATABASE IF EXISTS employees;
CREATE DATABASE employees;
\c employees
CREATE SCHEMA employees;
\q

pg_restore -h localhost -p 5432 -U postgres -d employees -v --no-owner --no-privileges -c "employees.sql"
psql -h localhost -p 5432 -U postgres -d employees

# Git clone

git clone https://github.com/papopporkingfujikuracloud1/backend-exam-database.git
