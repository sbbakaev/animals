# README #

### Description ###

**Level 1**:

* As a general requirement: Please make sure I can execute the code on my local machine, i.e. please provide all required dependencies and installation documentation or a ready to use build configuration, e.g. a maven pom.xml, composer etc if needed.
* Please write a program that reads file input.txt which you find attached to this mail.
* In this file you’ll find lines containing categories and data. The categories are “ANIMALS” and “NUMBERS”.
* Please note that categories are fix values, i.e. they are NOT determined by being written upper case.
* Each line following a category represents data items that belong to the previously read category (unless the new line represents a category itself)
* After reading and processing the file please output to the system console:
* A sorted list of all unique data items of category “ANIMALS”, i.e. ANIMALS:
```
cow
horse
moose
sheep
```

* A list of all unique data items of category “NUMBERS”, followed by “: “ and the number of occurrences of the respective data item, i.e.
```
one: 2
three: 2
two: 1
seven: 1
six: 2
```

**Level 2**:

* Read & process file „input2.txt“ which contains one more category called „CARS“.
* Data items are case insensitive, i.e. OPEL and Opel represent 1 unique data item
* Output the data for categories "ANIMALS" and "NUMBERS" as described in Level 1.
* Additionally, output the unique data items of category “CARS” as a backwards sorted list, each item written in lower case.
* Each data item output shall be followed by the item’s MD5 hash written in brackets.
* I.e. the expected output for CARS shall be:
```
vw (7336a2c49b0045fa1340bf899f785e70)
opel (f65b7d39472c52142ea2f4ea5e115d59)
bmw (71913f59e458e026d6609cdb5a7cc53d)
audi (4d9fa555e7c23996e99f1fb0e286aea8)
```
* Make sure the input file is read and processed only once.

**Level 3**:

* Provide phpUnit tests for your code.

**Level 4**:

* Do not use if/else, switch/case or Ternary Operations (http://en.wikipedia.org/wiki/Ternary_operation) in your code.
* The code should be written in a way that allows for adding new categories without changing the existing code base (open closed principle).

### Requirements ###
* php 5.6
* PHPUnit 5.2.12

### How do I get set up? ###

* Get sources:

```
$ git clone https://github.com/Respant/animals.git animals
```

* change directory

```
$ cd animals
```

* To run application: 
```
$ php index.php
```

* To run tests: 

```
$ phpunit
```

### To replace file: ###
* put new file in "files"
* change "fileName" in "app/config/config.php"

### To add new category: ###
* add new line for categories in "app/config/config.php" in format 'categoryKey' => 'categoryClass'
* create category class in "src/Classes/Category"
    * it should be named as categoryClass
    * it should implement \AG\Animals\Structure\CategoryInterface
* add phpunit tests for your class in "src/Tests/Category"


### Who do I talk to? ###
* **Anton Gobzhelyan**, anton.gobzhelyan@gmail.com
