# Laravel Hijri Date `Ummul Qura` Calendar
#  تحويل التواريخ من و إلى التاريخ الهجري حسب تقويم أم القرى 

[![License](https://poser.pugx.org/alkoumi/laravel-hijri-date/license)](https://packagist.org/packages/alkoumi/laravel-hijri-date)
[![Total Downloads](https://poser.pugx.org/alkoumi/laravel-hijri-date/downloads)](https://packagist.org/packages/alkoumi/laravel-hijri-date)
[![StyleCI](https://github.styleci.io/repos/229978322/shield?branch=master)](https://github.styleci.io/repos/229978322)


Laravel package to Convert laravel date to our Amazing 💝 Hjri date {ummul qura and vice versa} . to look like [ الخميس ، ٢٢ ربيع الآخر ، ١٤٤١ - ٠٧:٤٩ مساءً]
## Installation Up to Laravel 6

You can install the package via composer:

	composer require alkoumi/laravel-hijri-date

The service provider will automatically get registered. Or you may manually add the service provider in your `config/app.php` file:

    'providers' => [
        // ...
        Alkoumi\LaravelHijriDate\LaravelHijriDateServiceProvider::class,
    ];

## Usage

## Hijri Date `Ummul Qura` Calendar `[Short Format]`
You can simply get Ummul qura Hijri date directly in Short Format 
```php
    Hijri::DateShortFormat(); // RETURN Hijri Date of [NOW] Without Defining Timestamp

    [OR]

    $date = Carbon::now()->addMonth();
    Hijri::DateShortFormat($date); // RETURN Hijri Date of [$date] in Short Format
    // RESULT { 1441-04-27 }
```

## Hijri Date `Ummul Qura` Calendar `[Medium Format]`
You can simply get Ummul qura Hijri date directly in Medium Format 
```php
    Hijri::DateMediumFormat(); // RETURN Hijri Date of [NOW] Without Defining Timestamp

    [OR]

    $date = Carbon::now()->addMonth();
    Hijri::DateMediumFormat($date); // RETURN Hijri Date of [$date] in Medium Format
    // RESULT { الثلاثاء ، 27 ربيع الآخر ، 1441 }
```

## Hijri Date `Ummul Qura` Calendar `[Full Format]`
You can simply get Ummul qura Hijri date directly in Full Format 
```php
    Hijri::DateFullFormat(); // RETURN Hijri Date of [NOW] Without Defining Timestamp

    [OR]

    $date = Carbon::now()->addMonth();
    Hijri::DateFullFormat($date); // RETURN Hijri Date of [$date] in Full Format
    // RESULT { الثلاثاء ، 27 ربيع الآخر ، 1441 - 07:20:39 مساءً }
```

## Hijri Date `Ummul Qura` Calendar `[Your Custom Format]`
You can simply get Ummul qura Hijri date directly in Your Custom Format 
```php
    // Choose Your Format Like 'l ، j F ، Y'
    // Y => Hijri Year [1442]
    // F => Hijri Month Arabic Name [رمضان]
    // j => Hijri Day Number [27]
    // l => Arabic Day Name [الجمعة]
    // m => Hijri Month Number [09]
    // a => 'ص'
    // A => 'صباحًا'
    // H => Hour
    // i => Minutes
    // s => Seconds

    Hijri::Date('l ، j F ، Y'); // RETURN Hijri Date of [NOW] Without Defining Timestamp

    [OR]

    $date = Carbon::now()->addMonth();
    Hijri::Date('l ، j F ، Y', $date); // RETURN Hijri Date of [$date] in Full Format
```

