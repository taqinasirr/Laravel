```php
pa make:controller AyamController --resource
pa make:model Ayam -rmsfc
pa make:migration create_ayams_table
pa make:migration add_price_to_ayams_table
pa make:seeder AyamSeeder
pa make:auth

pa migrate rollback
pa migrate fresh --seed

pa db:seed --class=NamaSeeder
pa serve --port=8001
pa help
pa storage:link
pa route:list
pa tinker
pa list

```
