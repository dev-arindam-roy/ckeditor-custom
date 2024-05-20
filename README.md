# CK Editor - Custom Config

[https://dev-arindam-roy.github.io/ckeditor-custom/](https://dev-arindam-roy.github.io/ckeditor-custom/)

```js

//set content
CKEDITOR.instances[ 'pgb_ext_seo_edt' ].setData( _mainContent );
CKEDITOR.instances[ actionMidEleEdtId ].insertHtml('<div>' + galScode +'</div>');

//get content
CKEDITOR.instances.photo_gallery_content.on('blur', function() {
    var data = CKEDITOR.instances.photo_gallery_content.getData();
    if(data != '') {
      $('#perror').html('');
    }
});
CKEDITOR.instances.video_gallery_content.on('blur', function() {
    var data = CKEDITOR.instances.video_gallery_content.getData();
    if(data != '') {
      $('#verror').html('');
    }
});

CKEDITOR.instances[ accID ].updateElement(); //while form submit ajax

//ex
accrFrm.on('submit', function() {
    $('.accordion').each( function() { 
        var accID = $(this).attr('id');
        CKEDITOR.instances[ accID ].updateElement();
    } );
});

//ex
pgb_ext_cont_frm.on('submit', function() {
    CKEDITOR.instances.pgb_ext_cont_edt.updateElement();
});

//ex
fm.on('submit', function() {
  CKEDITOR.instances.pg_cont.updateElement();
});

//dynamic create or add more ck editor
CKEDITOR.replace( 'accr' + clMore, {
    customConfig: "{{ asset('public/assets/ckeditor/accr_config.js') }}",
});
clMore++;
```

[https://dev-arindam-roy.github.io/ckeditor-custom/](https://dev-arindam-roy.github.io/ckeditor-custom/)