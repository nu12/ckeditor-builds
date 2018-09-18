# Ckeditor::Builds

Gem to add CKEditor5 builds, for more information of usage, please visit [CKEditor's page](https://docs.ckeditor.com/ckeditor5/latest/)

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'ckeditor-builds'
```

And then execute:

    $ bundle install

Or install it yourself as:

    $ gem install ckeditor-builds

### Versions

Gem version matches CkEditor5 builds versions. For more information about the releases, please visit the [releases' page](https://ckeditor.com/blog/?category=releases&tags=CKEditor-5)

## Usage

Basic usage instructions below. For more information, please visit the [documentation](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/quick-start.html)

### Classic

In app/assets/javascripts/application.js
```ruby
//= require ckeditor-classic
```

In the view/HTML page
```html
<textarea name="content" id="editor">
    <p>This is some sample content.</p>
</textarea>

<script>
    ClassicEditor
    .create( document.querySelector( '#editor' ) )
    .catch( error => {
    console.error( error );
    } );
</script>
```

### Inline

In app/assets/javascripts/application.js
```ruby
//= require ckeditor-inline
```

In the view/HTML page
```html
<div id="editor">
    <p>This is some sample content.</p>
</div>
<script>
    InlineEditor
        .create( document.querySelector( '#editor' ) )
        .catch( error => {
            console.error( error );
        } );
</script>
```

### Balloon

In app/assets/javascripts/application.js
```ruby
//= require ckeditor-balloon
```

In the view/HTML page
```html
<div id="editor">
    <p>This is some sample content.</p>
</div>
<script>
    BalloonEditor
        .create( document.querySelector( '#editor' ) )
        .catch( error => {
            console.error( error );
        } );
</script>
```

### Document

In app/assets/javascripts/application.js
```ruby
//= require ckeditor-document
```

In the view/HTML page
```html
<!-- The toolbar will be rendered in this container. -->
<div id="toolbar-container"></div>

<!-- This container will become the editable. -->
<div id="editor">
    <p>This is the initial editor content.</p>
</div>

<script>
    DecoupledEditor
        .create( document.querySelector( '#editor' ) )
        .then( editor => {
            const toolbarContainer = document.querySelector( '#toolbar-container' );

            toolbarContainer.appendChild( editor.ui.view.toolbar.element );
        } )
        .catch( error => {
            console.error( error );
        } );
</script>
```

### Translations

Translations are editor-specific. In ```app/assets/javascripts/application.js```
```ruby
//= require translations/[classic|inline|balloon|document]/de
```

In the view/HTML page
```html
<script>
    ClassicEditor //InlineEditor|BalloonEditor|DecoupledEditor
    .create( document.querySelector( '#editor' ), {
        // The language code is defined in the https://en.wikipedia.org/wiki/ISO_639-1 standard.
        language: 'de'
    } )
    .then( editor => {
        console.log( editor );
    } )
    .catch( error => {
        console.error( error );
    } );
</script>
```

See [available languages](https://github.com/nu12/ckeditor-builds/tree/master/vendor/assets/javascripts/translations/classic)

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/nu12/ckeditor-builds.
