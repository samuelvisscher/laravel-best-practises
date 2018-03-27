# Best practises for Laravel

## Terminology

Resource: a specific model with database table in the system.

## Dev environment

### Homestead

Although users are free to use their own local environment, each project should have a homestead setup.

## API standards

All API routes are to be defined in `routes/api.php`.

### Authentication

In case an API requires authentication, we shall use oAuth2.0 through the Laravel Passport package.

Typically we use password grant tokens:

https://laravel.com/docs/5.6/passport#password-grant-tokens

Please review the documentation with regards to how we make authenticated requests.

### JSON

All communication between the front-end and back-end will occur through JSON requests.

## Development standards

When creating a new resource, please follow the following rules:

### Controllers

Controllers are placed within the `app/Http/Controllers` folder, unless a more specific folder has been created.

Use the following command: `php artisan make:controller NameOfModelController`

Only add methods (index, show, create, update and destroy), which are being exposed by `routes/api.php`.

### Model

Models are placed within the `app/Models` folder, and typically created together with their respective database tables.

Use the following command: `php artisan make:model Models/NameOfModel -m`

### Requests

All requests are placed within the `app/Http/Requests` folder, unless a more specific folder has been created.

Use the following command: `php artisan make:request NameOfModelCreate` or `php artisan make:request NameOfModelUpdate`.

### Tables

To be added ..

### Validators

All custom validators are placed within the `app/Rules`.

Use the following command: `php artisan make:rule NameOfRule`
