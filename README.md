## Laravel Excel v2.0.0 for Laravel 5

Looking for Laravel Excel for Laravel 4? Visit the [`1.3` branch](https://github.com/Maatwebsite/Laravel-Excel/tree/1.3)

[<img src="http://www.maatwebsite.nl/img/excel_banner.jpg"/>](http://www.maatwebsite.nl/laravel-excel/docs)

Laravel Excel brings the power of PHPOffice's PHPExcel to Laravel 5 with a touch of the Laravel Magic. It includes features like: importing Excel and CSV to collections, exporting models, array's and views to Excel, importing batches of files and importing a file by a config file.

- Import into Laravel **Collections**
- Export **Blade views** to Excel and CSV with optional CSS styling
- **Batch** imports
- A lot of optional **config settings**
- Easy **cell caching**
- Chunked importer
- ExcelFile method injections
- Editing existing Excel files
- **Advanced import** by config files
- and many more...

---

```php
Excel::create('Laravel Excel', function($excel) {

    $excel->sheet('Excel sheet', function($sheet) {

        $sheet->setOrientation('landscape');

    });

})->export('xls');
```

---

[![Build Status](https://travis-ci.org/Maatwebsite/Laravel-Excel.svg?branch=master)](https://travis-ci.org/Maatwebsite/Laravel-Excel)
[![Latest Stable Version](https://poser.pugx.org/maatwebsite/excel/v/stable.png)](https://packagist.org/packages/maatwebsite/excel) [![Total Downloads](https://poser.pugx.org/maatwebsite/excel/downloads.png)](https://packagist.org/packages/maatwebsite/excel)  [![License](https://poser.pugx.org/maatwebsite/excel/license.png)](https://packagist.org/packages/maatwebsite/excel)
[![Monthly Downloads](https://poser.pugx.org/maatwebsite/excel/d/monthly.png)](https://packagist.org/packages/maatwebsite/excel)
[![Daily Downloads](https://poser.pugx.org/maatwebsite/excel/d/daily.png)](https://packagist.org/packages/maatwebsite/excel)

#Installation

Require this package in your `composer.json` and update composer. This will download the package and PHPExcel of PHPOffice.

```php
"maatwebsite/excel": "~2.0.0"
```

After updating composer, add the ServiceProvider to the providers array in `app/config/app.php`

```php
'Maatwebsite\Excel\ExcelServiceProvider',
```

You can use the facade for shorter code. Add this to your aliases:

```php
'Excel' => 'Maatwebsite\Excel\Facades\Excel',
```

The class is bound to the ioC as `excel`

```php
$excel = App::make('excel');
```

To publish the config settings in Laravel 5 use:

```php
php artisan vendor:publish
```

This will add an `excel.php` config file to your config folder.

# Documentation

The complete documentation can be found at: [http://www.maatwebsite.nl/laravel-excel/docs](http://www.maatwebsite.nl/laravel-excel/docs)

# Contributing

**ALL** bug fixes should be made to appropriate branch (e.g. `2.0` for 2.0.* bug fixes). Bug fixes should never be sent to the `master` branch.

More about contributing can be found at: [http://www.maatwebsite.nl/laravel-excel/docs/getting-started#contributing](http://www.maatwebsite.nl/laravel-excel/docs/getting-started#contributing)

# License

This package is licensed under LGPL. You are free to use it in personal and commercial projects. The code can be forked and modified, but the original copyright author should always be included!