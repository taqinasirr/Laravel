### 1) Set faker kat factory

   i) UserFactory.php 
   
   ```php 
   'username' => $this->faker->unique()->userName(),
   ```

   ii) PostFactory.php  

   ```php
   return [
            'title' => $this->faker->sentence(mt_rand(2,8)),
            'slug' => $this->faker->slug(),
            'excerpt' => $this->faker->paragraph()
        ];   
   ``` 
   



### 2) Seeding


DatabaseSeeder.php
```php
          User::factory(3)->create();
          Post::factory(20)->create();
``` 


```php
pa db:seed
 atau
pa migrate:fresh --seed   (if nak fresh)	 
``` 
	
<br><br>


___
defaut password utk user adalah ‘password’  
Seeder = a special class used to generate and insert sample data (seeds) in a database.  

---
Each of the generator properties (like name, address) are called "formatters"  
cth formatters:  
  * userName()  
  * sentence()  
  * slug()  
  * paragraph()  
  * paragraphs()
  * dateTime()
  * bank()
  * bankAccountNumber
  * myKadNumber()
  * mobileNumber()
  * township()
  
  <br>

---
 tukar faker ke bahasa melayu  
  1. .env tambah ni  
    `FAKER_LOCALE=ms_MY`
  2) config/app.php  
  `'faker_locale' => 'en_US'`  
    ubah kepada  
  `'faker_locale' => env('FAKER_LOCALE','en_US'),`

  <br><br>

  > go to https://fakerphp.github.io/ utk tgk all available language & formatters      
