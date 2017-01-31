# jwt
JWT authorization wrapper for phramework, using firebase/php-jwt

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/15b80cc381f741ab8fc5af45bad02dc6)](https://www.codacy.com/app/NohponeX/jwt?utm_source=github.com&utm_medium=referral&utm_content=phramework/jwt&utm_campaign=badger)
[![Build Status](https://travis-ci.org/phramework/jwt.svg?branch=master)](https://travis-ci.org/phramework/jwt)

## Usage
Require package

```
composer require phramework/jwt
```

```php
//Set authentication class
\Phramework\Authentication\Manager::register(
    \Phramework\Authentication\JWT\JWT::class
);

//Set method to fetch user object, including password attribute
\Phramework\Authentication\Manager::setUserGetByEmailMethod(
    [\MyApp\API\Models\User::class, 'getByEmailWithPassword']
);

\Phramework\Authentication\Manager::setAttributes(
    ['user_type', 'email']
);
```

## Install dependencies

```bash
composer update
```

## Test and lint code

```bash
composer lint
composer test
```

# License
Copyright 2015 Xenofon Spafaridis

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

```
http://www.apache.org/licenses/LICENSE-2.0
```

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
