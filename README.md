# Standard Ruby Styleguide

We've started writing our Ruby code in the same way we do our JavaScript code and we've never been happier. We call this approach `srs`, because we're totally serious.

### Always use semicolons
End all your statements with semicolons. Semicolons are optional, but you should always put them in for consistency. Semicolons are fine in Ruby. All Ruby interpreters like MRI, Rubinius and JRuby will be able to parse your code correctly.

```rb
def create_user(name);
  user = User.create({ name: name });
  user.validate!();
  user.save();
end;
```

### Never omit parentheses
Although parentheses are optional in Ruby, prefer to always put them so that your code will be consistent.

```rb
# ✓ OK
if model.valid?();
  return model.save();
end;
```

```rb
# ✗ Wtf is this
if model.valid?
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

<br>

## FAQ

#### Is this actually valid Ruby?

**Yes, 100%.** There is a growing movement to enforce a semicolon-less style in languages like Ruby and Python. Don't believe the hype! Semicolons have existed [since 1494](https://en.wikipedia.org/wiki/Semicolon), and there's a good reason why Ruby's syntax allows semicolons. If it weren't necessary, then the language wouldn't have it, eh?

#### This is terrible advice.

That's not a question. Don't like semicolons in your semicolon-optional language? Start (or continue) writing them without semicolons, then! Start with [JavaScript](http://standardjs.com/rules.html) ;)

#### Are you really serious?

This document is satire in case you haven't picked up on that yet. If you want a real styleguide, look at [bbatsov/ruby-style-guide](https://github.com/bbatsov/ruby-style-guide).

<br>

[![](https://img.shields.io/badge/%E2%96%B6-Give_feedback-green.svg)](https://github.com/rstacruz/srs/issues/new)
