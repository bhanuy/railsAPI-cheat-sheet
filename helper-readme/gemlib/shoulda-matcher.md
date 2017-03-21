### Shoulda Matchers

*Shoulda Matchers provides RSpec- and Minitest-compatible one-liners that test common Rails functionality.*

## Getting started
### RSpec

Include `shoulda-matchers` in your Gemfile:

``` ruby
group :test do
  gem 'shoulda-matchers', '~> 3.1'
end
```

Now you need to tell the gem a couple of things:

* Which test framework you're using
* Which portion of the matchers you want to use

You can supply this information by using a configuration block. Place the
following in `rails_helper.rb`:

``` ruby
Shoulda::Matchers.configure do |config|
  config.integrate do |with|
    # Choose a test framework:
    with.test_framework :rspec
    with.test_framework :minitest
    with.test_framework :minitest_4
    with.test_framework :test_unit

    # Choose one or more libraries:
    with.library :active_record
    with.library :active_model
    with.library :action_controller
    # Or, choose the following (which implies all of the above):
    with.library :rails
  end
end
```

Now you can use matchers in your tests. For instance a model test might look
like this:

``` ruby
RSpec.describe Person, type: :model do
  it { should validate_presence_of(:name) }
end
```

### For more detail visit [shoulda-matchers]  https://github.com/thoughtbot/shoulda-matchers