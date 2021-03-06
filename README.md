# Notification Component
[![Version](https://img.shields.io/github/release/flextype-components/notification.svg?label=version)](https://github.com/flextype-components/notification/releases)
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://github.com/flextype-components/notification/blob/master/LICENSE)
[![Quality Score](https://img.shields.io/scrutinizer/g/flextype-components/notification.svg?branch=master)](https://scrutinizer-ci.com/g/flextype-components/notification?branch=master)

Notification component for storing and retrieving flash data.

### Installation

```
composer require flextype-components/notification
```

### Usage

```php
use Flextype\Component\Notification\Notification;
```

Initializes the Notification service.  
This will read notification/flash data from the `$_SESSION` variable and load it into
the $this->previous array.
```php
Notification::init();
```

Returns a specific variable from the Notifications array.
```php
echo Notification::get('success');
echo Notification::get('errors');
```

Adds specific variable to the Notifications array.
```php
Notification::set('success', 'Data has been saved with success!');
Notification::set('errors', 'Data not saved!');
```

Adds specific variable to the Notifications array for current page.
```php
Notification::setNow('success', 'Success!');
```

Clears the Notifications array.  
Data that previous pages stored will not be deleted, just the data that
this page stored itself.
```php
Notification::clean();
```

## License
See [LICENSE](https://github.com/flextype-components/notification/blob/master/LICENSE)
