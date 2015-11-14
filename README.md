# Standard Ruby Styleguide

We've started writing our **Ruby** code in the same way we do our **JavaScript** code and we've never been happier. We call this approach `srs`, because we're totally serious.

### Use semicolons on statements
End all your statements with semicolons. Semicolons are optional, but you should always put them in for consistency. Semicolons are fine in Ruby. All Ruby interpreters like MRI, Rubinius and JRuby will be able to parse your code correctly.

```rb
def create_user(name)
  user = User.create({ name: name });
  user.validate!();
  user.save();
end
```

### Only use semicolons on statements
Don't use semicolons on anything but statements. Lines that start or end blocks should have no semicolons.

```rb
class Warewolf < Wolf
  def bark
    puts('awoooo');
  end
end
```

It may be difficult to remember which things should have semicolons and which should not. Don't worry! There aren't many exceptions to remember. Just memorize this short list of keywords:

> `if` `unless` `elsif` `else` `while` `do` `end` `def` `class` `module` `begin` `rescue` `ensure` `catch` `case`

### Never omit parentheses
Although parentheses are optional in Ruby, prefer to always put them so that your code will be consistent.

```rb
# ✓ OK
role = :admin;
if model.valid_for?(role)
  return model.save();
end
```

```rb
# ✗ Wtf is this
role = :admin
if model.valid?(role)
  model.save
end
```

### Don't forget the curly braces
Inconsistency is the root of all evil. Even if they're inferred, prefer to be explicit with your curly braces around hashes. Why would you place your faith in Ruby's ACI (automatic curly-brace insertion)?

```rb
# ✓ OK
book = Book.new({ title: 'Pride & Prejudice', author: 'J. Austen' });
```

```rb
# ✗ This is terrible
book = Book.new(title: 'Pride & Prejudice', author: 'J. Austen')
```

```rb
# ✗✗✗ Seriously, do you even Ruby?
book = Book.new title: 'Pride & Prejudice', author: 'J. Austen'
```

### Write in other languages in the same way
Since we're trying to be consistent here, why limit yourself to just Ruby and JavaScript? Do the same with Python!

```py
class Dolphin:
    """Nothing can escape our love for semicolons.""";
    def bark(self):
        gimp = 'silly animal';
        print('I cannot bark, you ' + gimp);
```

<br>

## FAQ

#### Is this actually valid Ruby?

**Yes, 100%.** There is a growing movement to enforce a semicolon-less style in languages like Ruby and Python. Don't believe the hype! Semicolons have existed [since 1494](https://en.wikipedia.org/wiki/Semicolon), and there's a good reason why Ruby's syntax allows semicolons. If it weren't necessary, then the language wouldn't have it, eh?

#### Isn't it just easier to not put semicolons?

Yes. Actually it is.

#### Are you really serious?

This document is satire in case you haven't picked up on that yet. If you want a real styleguide, look at [bbatsov/ruby-style-guide](https://github.com/bbatsov/ruby-style-guide).

<br>

## What now?

`</satire>` — A lot of modern languages are semicolon-optional. This list includes Ruby, Python, JavaScript, Lua. In all but one of these languages, semicolons are recommended for use as a statement [separator](http://stackoverflow.com/questions/16862337/lua-semicolon-conventions#16863076) when including 2 statements in one line. JavaScript, on the other hand, has an abundancy of documentation that recommends all lines should be terminated with semicolons, despite it being only necessary as a statement separator.

Why not start writing your JavaScript without semicolons? If it's good enough for [npm](https://github.com/npm/npm/blob/master/lib/init.js), it's good enough for me :) Start by checking the [Standard JavaScript](http://standardjs.com/rules.html) style guide—I promise it'd bring much sanity to your development process.

<br>

[![](https://img.shields.io/badge/%E2%96%B6-Give_feedback-green.svg)](https://github.com/rstacruz/srs/issues/new)
