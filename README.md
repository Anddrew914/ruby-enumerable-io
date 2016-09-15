![General Assembly Logo](http://i.imgur.com/ke8USTq.png)

# Ruby Enumerable IO

## Instructions

Fork, clone, branch (training), and bundle install.

## Objectives

By the end of this lesson, developers should be able to:

-   Iterate through a file one line at a time.
-   Explain why you should only use the block form of `File.open`.
-   Load data using the CSV library in order to create Ruby objects.

## Introduction

In Ruby, files, and all IO streams, are Enumerable.

## Files as lists

Ruby's [File](http://ruby-doc.org/core-2.3.0/File.html) includes `Enumerable`
(via its **Parent** class [IO](http://ruby-doc.org/core-2.3.0/IO.html)) so we
can use all of the Enumerable methods to process files a character or a line
(the default) at a time.

Other enumerable classes related to working with files include **IO**, mentioned
above, and [Dir](http://ruby-doc.org/core-2.3.0/Dir.html).

We used the Ruby Standard Library class
[CSV](http://ruby-doc.org/stdlib-2.3.0/libdoc/csv/rdoc/CSV.html) to load data
for the `bin/*_array.rb` scripts in
[/ga-wdi-boston/ruby-vs-js-array-methods](https://github.com/ga-wdi-boston/ruby-vs-js-array-methods).

### Code along - read a file

Using `bin/read_file.rb` we'll read all the lines in a file and print them.

### Lab - count characters, words, and lines in a file

Let's create a script to mimic the behavior of the `wc` (word count) command
 line utility in `bin/word_count.rb`.

## CSV files

A file containing Comma Separated Values (CSV) is a simple and well supported
 format for data interchange, especially for tabular data.

### Code along - CSV

We'll build a data loader for pets in `lib/pets.rb` using the Ruby standard
 library class [CSV](http://ruby-doc.org/stdlib-2.3.0/libdoc/csv/rdoc/CSV.html).

We'll use a `lambda` - shorthand syntax `->([args]) {[code]}`, see
[Proc](http://ruby-doc.org/core-2.3.0/Proc.html) - to ensure we use properly
formatted symbols as keys when loading data.  In Ruby, lambdas verify the number
of arguments.  Alternatively, we could pass a symbol from
[HeaderConverters](http://ruby-doc.org/stdlib-2.3.0/libdoc/csv/rdoc/CSV.html#HeaderConverters)
as the value for `:header_converters` in the options Hash.

## Challenge

Read two files at the same time using `bin/read_files.rb`.

Look at [Enumerator](http://ruby-doc.org/core-2.3.0/Enumerator.html) which is
 what gets returned when we call `each` on an open file without a block.

We'll need to look briefly at [exception
handling](http://ruby-doc.org/core-2.3.0/Exception.html) as Enumerator relies on
this mechanism.

## [License](LICENSE)

1.  All content is licensed under a CC­BY­NC­SA 4.0 license.
1.  All software code is licensed under GNU GPLv3. For commercial use or
    alternative licensing, please contact legal@ga.co.
