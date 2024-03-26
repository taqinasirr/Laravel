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


```php
Ayam::create()

Ayam::all()
Ayam::get()
Ayam::latest()->get()
Ayam::latest()->paginate(5)
Ayam::with()
Ayam::find(1)
Ayam::findOrFail(2)
Ayam::firstWhere()
Ayam::where()->first()
Ayam::where->get()

Ayam::where('x', '=', 'y')
Ayam::where('x', 'y')
Ayam::where('x', '>', '10')

Post::where('id', $post->id)->update($validatedData)
$row()->update()

$row->delete()
destroy(1,2,3)
```

