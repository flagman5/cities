Using activerecord-import
===================

* This is an example showing usage of Zach Dennis' activerecord-import gem. Instead of playing with tutorial databases, I decided to create a somewhat real database that can be of use to all. I came across http://sourceforge.net/projects/zips/files/#files. 
* So, this is a simple Rails application (nothing there yet) with three models: City, Code and State. Some may argue if we need the models this way, but that's a separate thing. 
* What I wanted to do was use Zach Dennis' [excellent activerecord-import gem](https://github.com/zdennis/activerecord-import/wiki/) to see if I can seed the database with the zips.csv I have created (modified from original at sf.net). 
* Of course, the seeding should be fast. But more importantly, it should be correct. 
* So, I am going to ask Zach if he can take a look here.
---
After you clone this repository, just do the following:

* Modify database.yml to your environment.
* See db/seeds.rb. It has two methods: seed_from and import_from which I think seed the database correctly.
* See how import_from loses the API goodies of Rails AR to use models to modify database.
* But import_from is still way faster for such a trivial database of 33100 records. 
* My question to Zach is whether this is the right way to use activerecord-import gem. Of course, when I do this, I get *WARNING: Can't mass-assign protected attributes: id* all over, but I see no way around it.
