### factory_girls

factory_girl is a fixtures replacement with a straightforward definition syntax, support for multiple build strategies (saved instances, unsaved instances, attribute hashes, and stubbed objects), and support for multiple factories for the same class (user, admin_user, and so on), including factory inheritance.

Fixtures are a way of organizing data that you want to test against; in short, sample data. It allow you to automatically populate the database with data before each test.

# Drawbacks of fixture

  1. they are not easily modifiable, which tends to lead to duplicate fixtures
  2. They are typically loaded in mass by test frameworks.  This can be slow if many unnecessary fixtures are being loaded for each unit test.

### ```factory_girl_rails``` provides Rails integration for factory_girl.

### For more detail visit [factory_girl](https://github.com/thoughtbot/factory_girl)