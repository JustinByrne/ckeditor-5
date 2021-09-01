# ckeditor-5

Built from source ckeditor 5. To use this version add `./build/ckeditor.js` to your project then add the below to the bottom of any page you are wanting to use, then add the `editor` class to any textarea to initate.

```js
ClassicEditor
    .create( document.querySelector( '.editor' ), {
        toolbar: {
            items: [
                'heading',
                '|',
                'bold',
                'italic',
                'link',
                'bulletedList',
                'numberedList',
                '|',
                'alignment',
                'outdent',
                'indent',
                '|',
                'horizontalLine',
                'imageUpload',
                'blockQuote',
                'insertTable',
                'undo',
                'redo',
                '|',
                'code',
                'codeBlock',
                'sourceEditing'
            ]
        },
        language: 'en-gb',
        image: {
            toolbar: [
                'imageTextAlternative',
                'imageStyle:inline',
                'imageStyle:block',
                'imageStyle:side'
            ]
        },
        table: {
            contentToolbar: [
                'tableColumn',
                'tableRow',
                'mergeTableCells'
            ]
        },
    } )
    .then( editor => {
        window.editor = editor;
    } )
    .catch( error => {
        console.error( 'Oops, something went wrong!' );
        console.error( 'Please, report the following error on https://github.com/ckeditor/ckeditor5/issues with the build id and the error stack trace:' );
        console.warn( 'Build id: ev8x3bvarobq-2wtseetmv2wp' );
        console.error( error );
    } );
```