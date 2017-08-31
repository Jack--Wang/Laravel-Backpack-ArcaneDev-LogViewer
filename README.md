# Laravel-Backpack-ArcaneDev-LogViewer

Integrate [ArcaneDev/LogViewer](https://github.com/ARCANEDEV/LogViewer) in your [Laravel-Backpack](https://github.com/Laravel-Backpack/Base) project

![screenshot](https://user-images.githubusercontent.com/4065733/29937863-8b9bee30-8e4c-11e7-958f-534896cc230f.png)

# Requirements

All you neeed is Laravel-Backpack/Base (you don't need their Laravel-Backpack/LogManager)

https://github.com/Laravel-Backpack/Base

# Install ArcaneDev/LogViewer

https://github.com/ARCANEDEV/LogViewer

## Install package

	composer require arcanedev/log-viewer

## Add providers

	'providers' => [
	    ...
	    Arcanedev\LogViewer\LogViewerServiceProvider::class,
	],

## Publish log-viewer views

	php artisan log-viewer:publish

## Important! you must have a daily log

go to config/app.php and and set it like this

	'log' => 'daily',


## Replace views

Replace log-viewer views with the ones in this package

	resources/views/vendor/log-viewer/

## Add a link to your backpack sidebar

go to 

	resources/views/vendor/backpack/base/inc/sidebar.blade.php

add this line 

	<li><a href="{{ route('log-viewer::logs.list') }}"><i class="fa fa-info-circle"></i> <span>Log Viewer</span></a></li>




