Example lecture on Ruby hashes
======================

This lesson plan follows the LEARN Model.

# Objective
Students will be able to...
- Level 1 (Recall)
  - identify hashes when they see them
  - define hashes and nested hashes containing different datatypes as keys and values
- Level 2 (Skill/Concept)
  - categorize hashes in the context of other datatypes
  - distinguish hashes from other datatypes
- Level 3 (Strategic Thinking)
  - draw conclusions on when to use hashes

# Link
- A hash is just another Ruby datatype like all the others we have learned about
- Using hashes is more contextual and semantic than using arrays, so it will make your lives as programmers much easier

# Educate and Engage & Active Learning
## Hash Notation

Where you saw arrays using square brackets (`[]`), hashes use curly braces (`{}`).

## Creating Hashes
Ways to create hashes:

```ruby
 a = Hash.new
 => {}
 
 a = {}
 => {}
```

## Assigning Hash Values

Hashes follow the `key => value` pattern. The key should hold a description about the information it is holding, the value is the information itself.

```ruby
john = { age: 22 }
=> {:age=>22}
```

In the example above, a symbol is used as key, and an integer as value. Keys and values can be any datatype. Symbols are often used as keys because they are memory efficient.

**Does that make sense?**

A hash can hold a lot of information:

```ruby
john = {
  age: 22,
  first_name: 'John',
  last_name: 'Doe',
  address: [-12.234234,54.454565]
}
```

**Fist to five**

## Retrieving hash values

To retrieve a value from a hash, make use of square brackets and pass in the key whose value you are looking for.

```ruby
john = { age: 22 }
john[:age]
 => 22
```

Values can be overriden:

```ruby
john = { age: 22 }
john[:age] = 50

john
 => {:age=>22}
john[:age]
 => 50
```

## Nested Hashes

Values of hashes can be hashed themselves. Access to values is nested accordingly.

```ruby
people = {
  john: { age: 22 },
  lisa: { age: 21 }
}

people[:john]
 => {:age=>22}
 
people[:john][:age]
 => 22
```

**Fist to five**

## Hash Methods
Hashes come with many helpful methods than can be used to work with them or manipulate them.

Some examples:

`hash.clear` - Removes all key-value pairs from hash

`hash.delete(key)` - Deletes a key-value pair from hash by key

`hash.each { |key,value| block }` - Iterates over hash, calling the block once for each key, passing the key-value as a two-element array

`hash.has_key?(key) [or] hash.include?(key)` - Tests whether hash contains the given key

`hash.has_value?(value)` - Tests whether hash contains the given value

`hash.keys` - Creates a new array with keys from hash

`hash.length` - Returns the size or length of hash as an integer

`hash.values` - Returns a new array containing all the values of hash

**Explain in your own words**

# Reflect
**Exercise: Define a hash that contains five different animals and different information about them (color, age, etc). One of the values should be a hash itself (nested hash). Store your hash in a variable and find out/do the following in your Ruby console:**

- How many elements does your hash contain?
- List all keys and sort them alphabetically
- List all values
- Check if your hash contains an item with the key of `:not_present`
- Iterate over your hash and print all keys with their values (advanced: deeply nested)

**Ask one student to present their solution**

# Now and Then
What we covered in this lecture is very important because we will use hashes repeatedly throughout the course from here on out. Using hashes will make your Ruby programs easier to write and understand.

For more information, refer to:

- http://www.tutorialspoint.com/ruby/ruby_hashes.htm
- http://www.ruby-doc.org/core-2.1.4/Hash.html
