# Cqslight

Welcome to your new gem! In this directory, you'll find the files you need to be able to package up your Ruby library into a gem. Put your Ruby code in the file `lib/cqslight`. To experiment with that code, run `bin/console` for an interactive prompt.

TODO: Delete this and the text above, and describe your gem

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'cqslight'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install cqslight

## Usage

You can implement command classes such as:

```ruby
class RegisterUserCommand
  include Cqslight::Command

  def initialize(params)
  end

  def run
    # TODO: You need to implement a command process.
  end
end
```

and use it by such following code.

```ruby
class UsersController < ActionController
  def create
    command = RegisterUserCommand.run(params)
    if command.success?
      render
    else
      render :new
    end
  end
end
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/cqslight.

