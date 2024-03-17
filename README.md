# Laravel Blade Directives

Blade is a powerful templating engine provided with Laravel for working with PHP and HTML. It provides various directives to make your views more expressive and concise.

## Control Structures

### @if

The `@if` directive is used for conditional statements.

```php
@if($condition)
    // code to execute if condition is true
@elseif($anotherCondition)
    // code to execute if another condition is true
@else
    // code to execute if none of the conditions are true
@endif
```

### @foreach

The `@foreach` directive is used to iterate over arrays or objects.

```php
@foreach($items as $item)
    // code to execute for each item
@endforeach
```

### @for

The `@for` directive is used for simple loop iterations.

```php
@for($i = 0; $i < 5; $i++)
    // code to execute for each iteration
@endfor
```

### @while

The `@while` directive is used for indefinite loop iterations.

```php
@while($condition)
    // code to execute while the condition is true
@endwhile
```

### @empty

The `@empty` directive checks if a variable is empty.

```php
@empty($variable)
    // code to execute if the variable is empty
@endempty
```

## Outputting Data

### `{{}}`

The `{{ }}` directive is used to echo the contents of a variable.

```php
{{ $variable }}
```

### `{{!! !!}}`

The `{!! !!}` directive outputs the contents without escaping HTML entities.

```php
{!! $htmlContent !!}
```

## Including Sub-Views

### @include

The `@include` directive is used to include a sub-view.

```php
@include('view.name')
```

## Extending Layouts

### @extends

The `@extends` directive is used to inherit a layout.

```php
@extends('layout.name')
```

### @section

The `@section` directive defines a section that can be overwritten in child views.

```php
@section('sectionName')
    // content of the section
@endsection
```

### @yield

The `@yield` directive is used to output the contents of a section.

```php
@yield('sectionName')
```

### @parent

The `@parent` directive is used to display the content of the parent section.

```php
@section('sectionName')
    @parent
    // additional content
@endsection
```

## Comments

### `{{-- --}}`

The `{{-- --}}` directive is used to add comments in Blade templates.

```php
{{-- This is a blade comment --}}
```

## Authentication Directives

### @auth

The `@auth` directive checks if the user is authenticated.

```php
@auth
    // code to execute if the user is authenticated
@endauth
```

### @guest

The `@guest` directive checks if the user is a guest.

```php
@guest
    // code to execute if the user is a guest
@endguest
```

## Authorization Directives

### @can

The `@can` directive checks if the user has a certain permission.

```php
@can('permissionName')
    // code to execute if the user has the permission
@endcan
```

### @cannot

The `@cannot` directive checks if the user does not have a certain permission.

```php
@cannot('permissionName')
    // code to execute if the user does not have the permission
@endcannot
```

## Environment Directives

### @env

The `@env` directive checks the application environment.

```php
@env('local')
    // code to execute if the application is in the local environment
@endenv
```

### @production

The `@production` directive checks if the application is in production environment.

```php
@production
    // code to execute if the application is in production environment
@endproduction
```
