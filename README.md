# dev_Stata-to-Spark
Stata to Spark Workspace and Notes

#### JDBC Notes
- Loading JDBC
  ```
  . local jar "redshift-jdbc42-2.0.0.0.jar"
  . local driverc "com.amazon.redshift.jdbc42.Driver"
  . local url "jdbc:redshift://redshift-cluster-1.cziajbxjzi3e.us-west-2.redshift.amazonaws.com:5439/testdb"
  . local user "testuser"
  . local pass "secret"

  . jdbc add TestDB,  jar("`jar'") driverclass("`driverc'") url("`url'")
        user("`user'") password("`pass'")
  ```

- Connect to DB
  ```
  . jdbc connect TestDB
  ```

- Get Table(s) Info
  ```
  . jdbc showtables

  . jdbc describe <table>
  ```

#### Integration with Jupyter
- Jupyter Notebook with Stata
  [https://www.stata.com/new-in-stata/jupyter-notebooks/](https://www.stata.com/new-in-stata/jupyter-notebooks/) </br>

- Stata Kernel
  [https://kylebarron.dev/stata_kernel/](https://kylebarron.dev/stata_kernel/) <br/>
