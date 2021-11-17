# cube.js mysql driver (some bugfix)

>  for better support mysql like database (oceanbase....)



## Usage


```code
const {MySqlDriver,MySqlQuery} = require("@dalongrong/mymysql-driver")
module.exports = {
    dialectFactory: (dataSource) => {
        // need config  datasource  for multitenant env
        return MySqlQuery
    },
    dbType: ({ dataSource } = {}) => {
        return "mymysql"
    },
    driverFactory: ({ dataSource } = {}) => {
        return new MySqlDriver({})
    }
};
```