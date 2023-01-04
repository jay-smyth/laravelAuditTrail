# laravelAuditTrail

With this application we can use the database table relationships to determine an audit trail, the problem was, role level determined when and by whom data could be altered/verified ok after update.  

Eloquent queries combined with some object based looped functions are used to determine updates to the object data in it's preffered table, then they are either straight away distributed to the relevant table or stored in a pending authorization table, the purpose of the authorization table is to allow admins time to review the changes made by less premitted roles and verify the changes were sound, additionally any changes made to any data within certian tables had to be stored in an archive for the audt trail. 

#Laravel build commands
````
composer composer create-project laravel/laravel .  //download to the current working directory
````

#Required packages

Spatie Laravel-permission
````
composer require spatie/laravel-permission
````

