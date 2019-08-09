# Array Methods

## Learning Goals

- Sort an `Array`
- Reverse an `Array`
- Find the first and last elements of an `Array`
- Find out if an element is in an `Array`
- Find the size of an `Array`

## Introduction

We can now create an `Array`, as well as add to and remove items from an `Array`.
Next we'll take a closer look at other methods we can use with `Array`s, including
how to sort elements in an `Array`, how to find an element in an `Array` and how to
determine the size of an `Array`.

## Sort an Array

Sometimes we need to rearrange the contents of an `Array` in a certain order: for
strings, this means alphabetically, and for numerical values, this means from
smallest number to highest number.

```ruby
famous_cats = ["lil' bub", "grumpy cat", "maru"]
famous_cats.sort => ["grumpy cat", "lil' bub", "maru"]
famous_cats #=> ["lil' bub", "grumpy cat", "maru"]
```

The `sort` method ***returns a new `Array`*** with the elements of the `Array`
it was called upon sorted.  Here we see that the return value of `famous_cats`
remains unchanged after using the `sort` method on it. `sort` returns an
entirely new `Array`.  Because `sort` returns a new `Array`, we generally store
it in another variable.

```ruby
sorted_cats = famous_cats.sort
```

Now we have two copies of the `Array`. One unsorted (`famous_cats`) and one sorted
(`sorted_cats`).

If you don't need the unsorted version of the `Array` you can call `sort!`.
This will sort the existing `Array` without requiring you to save the return
into a new variable. The `!` (called "bang") is a Ruby convention that
indicates the method will do the operation _in place_. It will modify the
_receiver_ of the method (or the thing to the left of the dot).

When starting out, we recommend _not_ using the `sort!` method for
readability's sake. This helps in readability as when we're later working with
`sorted_names` we know we don't need to sort the `Array` again.

## Reverse an Array

What if we want to arrange the elements in an `Array` in the opposite order? For that, we
use the `.reverse` method.

```ruby  
famous_wizards = ["Dumbledore", "Gandalf", "Merlin"]
famous_wizards.reverse
  => ["Merlin", "Gandalf", "Dumbledore"]
```

Similarly to `sort` and `sort!`, when we call `reverse!` we are modifying the
receiver of the method in place while `reverse` returns a new `Array`.

## Find the First and Last Elements of an Array

We've got two ***extremely useful*** methods that give us the first and last
elements of an `Array`.

The `.first` method will return the _first_ element of an `Array`. As with the
other methods we've seen here, it does not change the return value of the
original `Array`.

```ruby
famous_cats = ["lil' bub", "grumpy cat", "Maru"]
famous_cats.first
  => "lil' bub"
```

The `.last` method will return the _last_ element of an `Array`. It also does not
change the return value of the original `Array`.

```ruby
famous_cats = ["lil' bub", "grumpy cat", "Maru"]
famous_cats.last
  => "Maru"
```

> **DEEPER THINKING**: Why not just use `[0]` or `[-1]` you might ask. The
> answer is aesthetics and communication. While we know `[0]` means "the first
> element," `.first` more clearly _suggests_ that the `Array` has been sorted
> and that the `0`th element was not put there by chance but because it's
> special. The same logic applies to `.last`. Thinking about subtle
> communication hints is something that you'll grow more comfortable with over
> time.

## Find Out If an Element Is in an Array

It's helpful to know whether  a particular element is in a given `Array`. For
example, does the `famous_cats` `Array` contain our favorite famous cat? We can
use the `.include?` method to find out.

The `.include?` method will return a boolean of whether or not the `Array`
contains (or ​_includes_) the element submitted to it inside the parentheses.

```ruby
famous_cats = ["lil' bub", "grumpy cat", "Maru"]
famous_cats.include?("Garfield")
#=> false
famous_cats.include?("Maru")
#=> true
```

Garfield is not in this `famous_cats` `Array`. Since we are just returning
`true` or `false`, the receiver of the method, `famous_cats`, remains
unchanged.

## Find the Size of an Array

Sometimes we need a quick way to know how large an `Array` is. In those cases we
can use the `.size` method, which will return the number of elements in the
`Array`.

```ruby
famous_cats = ["lil' bub", "grumpy cat", "Maru"]
famous_cats.size
  => 3
```

Even though `Array`s start with a 0 `index`, this method returns the actual number
of elements, starting from 1.

## Conclusion

There are a number of methods we can use to rearrange, retrieve and count
elements in an `Array`. With `.sort`, `.reverse`, `.first`, `.last`,
`.include?` and `.size`, we can easily get the information from an `Array` that
we need.

## Resources

- [Ruby Docs: Array](https://ruby-doc.org/core-2.2.0/Array.html)
