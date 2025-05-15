## Projects

### Common Lisp

**[cl-dbi-connection-pool](https://github.com/tamurashingo/cl-dbi-connection-pool)**

connection pool for CL-DBI

<details>
```common-lisp
(setf *connection-pool* (make-db-connection-pool :mysql
                                                 :database-name "dbicp_dev"
                                                 :username "root"
                                                 :password "password"
                                                 :host "mysql-test"
                                                 :port 3306))


(let ((conn (get-connection *connection-pool*)))
  (prog1
    (do-sql conn "SELECT * FROM USERS")
    (disconnect conn)))
```
</details>


**[cl-batis](https://github.com/tamurashingo/cl-batis)**

SQL Mapping Framework

<details>
```common-lisp
(setf *session* (create-sql-session :mysql
                                    :database-name "batis_dev"
                                    :username "root"
                                    :password "password"
                                    :host "mysql-test"
                                    :port 3306))


@update ("insert into product (id, name, price) values (:id, :name, :price)")
(defsql register-product (id name price))

(update-one *session* register-product :id 1 :name "NES" :price 14800)
```
</details>


**[reddit1.0](https://github.com/tamurashingo/reddit1.0)**

rewrite old reddit

<details>
```sh
make setup

make dev.up

curl -v http://localhost:8000/browse
```
</details>


### Java


**[dbutils3](https://github.com/tamurashingo/dbutils3)**

database utility


**[sql-analyzer](https://github.com/tamurashingo/sql-analyzer)**

generate SQL and params for prepared statement


