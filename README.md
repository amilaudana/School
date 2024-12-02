# <div align="center">mSchool</div>
<div align="center" dir="auto">
<img alt="GitHub License" src="https://img.shields.io/github/license/amilaudana/student"> 
<img src="https://img.shields.io/badge/magento-2-blue.svg?logo=magento&longCache=true" alt="Magento 2 Supported Version">
</div>

## <div align="center">CodeAesthetix School Module</div>  
<div align="center" dir="auto">
<img src="https://img.shields.io/badge/school-1.0.0-blue.svg?logo=magento&longCache=false&style=for-the-badge" alt="Magento 2 Supported Version">
</div>

### Overview
The CodeAesthetix School module is a custom Magento 2 module designed to manage School records within the Magento Admin Panel. It provides administrators with tools to add, update, delete, and associate Schools with specific stores, leveraging Magento 2's best practices such as Service Contracts, UI Components, and Dependency Injection.

### Features
Admin UI for managing School data (Add, Edit, Delete).
Store association for Schools to handle multi-store environments.
Logging and validation for secure data handling.
Grid-based School management with filtering and sorting options.
Modular architecture following Magento 2 coding standards.

### Requirements
Magento Version: Magento 2.4.x

PHP Version: PHP 8.x

### Installation
Clone the Repository:
Clone the repository into the app/code/CodeAesthetix/School directory:

```
git clone <repository-url> app/code/CodeAesthetix/School
```
Enable the Module:
Run the following Magento commands to enable the module:

```
php bin/magento module:enable CodeAesthetix_School
php bin/magento setup:upgrade
php bin/magento setup:di:compile
```
Flush Cache:
Clear the Magento cache to apply changes:

```
php bin/magento cache:flush
```

### Usage
#### Admin Form
The School module provides an admin form for adding or editing School records:

Go to School > Manage Schools in the Magento Admin Panel.

From here, you can:

Add new Schools with fields such as First Name, Last Name, Age, and Description.
Associate Schools with specific stores.
Manage Schools Grid
The module includes a grid for managing School records:

View all Schools, filter by specific criteria, and sort columns.
Perform inline editing for quick updates.

### Key Components
#### Service Contracts
The module uses Magento 2 service contracts to handle School data operations.

CodeAesthetix\School\Api\Data\SchoolInterface: Interface defining the School entity.

CodeAesthetix\School\Api\SchoolRepositoryInterface: Interface for CRUD operations on School data.

#### UI Components
The admin panel leverages Magento 2’s UI Components:

ui_component/School_form.xml: Defines the admin form layout and fields.
ui_component/School_listing.xml: Defines the School management grid.

#### Resource Models
The module uses resource models to handle database operations:

CodeAesthetix\School\Model\ResourceModel\School: Resource model for the School_entity table.
CodeAesthetix\School\Model\ResourceModel\School\Collection: Handles collections of School entities.

#### Logging
The module includes logging for operations like creating, updating, and deleting Schools, ensuring secure data handling and easy debugging.

### Testing
Unit Tests
The module includes unit tests for key components such as repositories and models.

Run the tests using PHPUnit:

```
vendor/bin/phpunit app/code/CodeAesthetix/School/Test/Unit
```
### Troubleshooting
If you encounter any issues:

Ensure the module is enabled:

```
php bin/magento module:status
```

Check logs in the var/log directory for detailed error messages:

var/log/system.log
var/log/exception.log
Verify database integrity:
Ensure all foreign key constraints are satisfied, and the schema matches the module requirements.

### License
This module is licensed under the MIT License.
