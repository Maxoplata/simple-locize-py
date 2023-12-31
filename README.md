# Simple Locize

Simple Locize is a library for handling translations via the Locize API. Locize is a translation management system that allows you to easily manage your application's translations.

## Installation

```sh
pip install simple-locize
```

## Usage

To use Simple Locize, you first need to create an instance of the `SimpleLocize` class:

```python
from simple_locize import SimpleLocize

project_id = 'your-project-id'
environment = 'your-environment'
private_key = 'your-private-key' # optional

locize = SimpleLocize(project_id, environment, private_key)
```

### Fetching translations

To fetch translations for a specific namespace and language, you can use the `get_all_translations_from_namespace` method:

```python
namespace = 'your-namespace'
language = 'en'

translations = locize.get_all_translations_from_namespace(namespace, language)
```

This will return an object containing all translations for the specified namespace and language.

### Translating a key

To translate a specific key for a namespace and language, you can use the `translate` method:

```ruby
namespace = 'your-namespace'
language = 'en'
key = 'your.key'

translation = locize.translate(namespace, language, key)
```

This will return the translation for the specified key, or the key itself if no translation is found.

## License

Simple Locize is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
