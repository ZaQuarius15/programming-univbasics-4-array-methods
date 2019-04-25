# Array Methods

## Learning Goals

- Sort an array
- Reverse an array
- Find the first and last elements of an array
- Find out if an element is in an array
- Find the size of an array

## Introduction

We can now create an array, as well as add to and remove items from an array.
Next we'll take a closer look at other methods we can use with arrays, including
how to sort elements in an array, how to find an element in an array and how to
determine the size of an array.

## Sort an Array

Sometimes we need to rearrange the contents of an array in a certain order: for
strings, this means alphabetically, and for numerical values, this means from
smallest number to highest number.

```ruby
famous_cats = ["lil' bub", "grumpy cat", "maru"]
famous_cats.sort
  => ["grumpy cat", "lil' bub", "maru"]
```

Here we see that the return value of `famous_cats` remains unchanged after using
the `sort` method on it. If you call `famous_cats` again after the sort, it will
still return `["lil' bub", "grumpy cat", "maru"]`, not the previously sorted
array. `sort` returns an entirely new array.

Because `sort` returns a new array, we generally store it in another variable.

```ruby
sorted_cats = famous_cats.sort
```

Now we have two copies of the array. One unsorted (`famous_cats`) and one sorted
(`sorted_cats`).

If you don't need the unsorted version of the array you can call `sort!`. This
will sort the existing array without requiring you to save the return into a new
variable. The `!` (called "bang") is a Ruby convention that indicates the method will do the
operation _in place_. It will modify the _receiver_ of the method (or the thing
to the left of the dot).

## Reverse an Array

What if we want to arrange the elements in an array in the opposite order? For that, we
use the `.reverse` method.

```ruby  
famous_wizards = ["Dumbledore", "Gandalf", "Merlin"]
famous_wizards.reverse
  => ["Merlin", "Gandalf", "Dumbledore"]
```

Similarly to `sort!`, when we call `reverse!` we are modifying the receiver of
the method in place.

## Find the First and Last Elements of an Array

We've got two useful methods that give us the first and last elements of an
array.

The `.first` method will return the _firs_ element of an array. As with the
other methods we've seen here, it does not change the return value of the
original array.

```ruby
famous_cats = ["lil' bub", "grumpy cat", "Maru"]
famous_cats.first
  => "lil' bub"
```

The `.last` method will return the _last_ element of an array. It also does not
change the return value of the original array.

```ruby
famous_cats = ["lil' bub", "grumpy cat", "Maru"]
famous_cats.last
  => "Maru"
```

## Find Out If an Element Is in an Array

Wondering if a particular element is in a given array? For example, does the
`famous_cats` array contain our favorite famous cat? We can use the `.include?`
method to find out.

The `.include?` method will return a boolean of whether or not the array
contains (or ​_includes_) the element submitted to it inside the parentheses.

```ruby
famous_cats = ["lil' bub", "grumpy cat", "Maru"]
famous_cats.include?("Garfield")
  => false
famous_cats.include?("Maru")
  => true
```

Unfortunately, Garfield is not in this `famous_cats` array. Since we are just
returning `true` or `false`, the receiver of the method, `famous_cats`, remains
unchanged.

## Find the Size of an Array

Sometimes we need a quick way to know how large an array is. In those cases we
can use the `.size` method, which will return the number of elements in the
array.

```ruby
famous_cats = ["lil' bub", "grumpy cat", "Maru"]
famous_cats.size
  => 3
```

Even though arrays start with a 0 `index`, this method returns the actual number
of elements, starting from 1.

**Note**: Remember that all of the methods here are case sensitive. For example,
`reverse` not `Reverse`.

## Conclusion

There are a number of methods we can use to rearrange, retrieve and count
elements in an array. With `.sort`, `.reverse`, `.first`, `.last`, `.include?`
and `.size`, we can easily get the information from an array that we need.

## Resources

- [Ruby Docs: Array](https://ruby-doc.org/core-2.2.0/Array.html)
