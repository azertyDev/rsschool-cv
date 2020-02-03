# 1. First Name, Last Name
_Khikmatov Umid_
# 2. Contact Info
1. _Phone:_ *+998909504960*
2. _Email_: *<khikmatovumid@gmail.com>*
3. _Github:_ [azertyDev](https://github.com/azertyDev "My github page")
# 3. Summary
> Results-oriented software engineer with a focus on the design and implementation of relational database systems. 2 years of experience in developing cutting-edge engineering solutions with a wide range of eCommerce and technology features. Skilled in backend and frontend development, and creating eCommerce websites that integrate with Paypal, Stripe and other payment APIs.

# 4. Skills
- The usual languages:
   - Javascript
- Database applications:
   - MySQL
   - PostgreSQL
   - MongoDB
   - Oracle
- Operating systems:
   - Windows
   - Linux/Unix
- Web applications:
   - HTML
   - CSS
   - React
- Frameworks and Libraries:
  - React
  - Bootstrap
- Tools:
  - GIT 
  - VS Code  
  - Webstorm 

# 5. Code examples

    const express = require('express');
    const router = express.Router();
    const mysql = require('mysql');
    const config = require('../config/config').db;

    // Connect to db
    function handleDisconnect() {
    connection = mysql.createConnection(config); 
    connection.connect(function(err) {
        if(err) {
            console.log('error when connecting to db');
            setTimeout(handleDisconnect, 604800);
        }
        connection.on('error', function(err) {
            if(err.code === 'PROTOCOL_CONNECTION_LOST') { 
                handleDisconnect();
            } else {
                throw err;
            }
        });
    })
    }
    handleDisconnect();

    router.get('/', (req, res, release) => {
    connection.query('SELECT * FROM red_wine', (err, data) => {
        if (err) {
            console.log("Error in the query");
        } else {
            res.render('./pages/wine', {title: 'Wine dataset', result: data, condition: true});
        }
    });
    });

    module.exports = router;

# 6. Experience

> Source code from my github repository:
>
>> [HR-Bot](https://github.com/azertyDev/hr-bot)
> 
>> [RentCar](https://github.com/azertyDev/RentCar)
> 
>> [MyBrary](https://github.com/azertyDev/Mybrary)

# 7. Education

### _Master student at Tashkent University of Information Technology_

# 8. English
### Level: Intermediate