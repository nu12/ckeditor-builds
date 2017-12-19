# Ckeditor::Builds

Gem to add CKEditor5 builds, for more information of usage, please visit https://docs.ckeditor.com/ckeditor5/latest/

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'ckeditor-builds'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install ckeditor-builds

## Usage

Edit app/assets/javascript/application.js

### Classic
```ruby
(...)
//= require ckeditor-classic
(...)

ClassicEditor
.create( document.querySelector( '#editor' ) )
.then( editor => {
    console.log( editor );
} )
.catch( error => {
    console.error( error );
} );
```

```html
<textarea name="content" id="editor">
    <p>Here goes the initial content of the editor.</p>
</textarea>
```

### Inline
```ruby
(...)
//= require ckeditor-inline
(...)

InlineEditor
.create( document.querySelector( '#editor' ) )
.then( editor => {
    console.log( editor );
} )
.catch( error => {
    console.error( error );
} );
```

```html
<div id="editor">
    <p>Here goes the initial content of the editor.</p>
</div>
```

### Balloon
```ruby
(...)
//= require ckeditor-balloon
(...)

BalloonEditor
.create( document.querySelector( '#editor' ) )
.then( editor => {
    console.log( editor );
} )
.catch( error => {
    console.error( error );
} );
```

```html
<div id="editor">
    <p>Here goes the initial content of the editor.</p>
</div>
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/nu12/ckeditor-builds.
