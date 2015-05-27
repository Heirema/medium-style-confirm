## medium-style-confirm

### Demo @ [bitwiser.in](http://bitwiser.in/medium-style-confirm/)

### Usage

* `mscConfirm(title, okCallback)` :
```js
mscConfirm("Delete?",function(){
    alert("Post deleted");
});
```

* `mscConfirm(title, subheading, okCallback)` :
```js
mscConfirm("Delete", "Are you sure you want to delete this post?", function(){
    alert("Post deleted");
});
```

* `mscConfirm(title, subheading, okCallback, cancelCallback)` :
```js
mscConfirm("Delete", "Are you sure you want to delete this post?", function(){
  alert("Post deleted");
},
function() {
  alert('Cancelled');
});
```

* `mscConfirm(object)` :
```js
mscConfirm({
    title: 'License',
    subtitle: 'Do you accept the licese agreement?',    // default: ''
    okText: 'I Agree',      // default: OK
    cancelText: 'I Dont',   // default: Cancel
    dismissOverlay: true,   // default: false, closes dialog when clicked on overlay.
    onOk: function() {
        alert('Awesome.');
    },
    onCancel: function() {
        alert('Sad face :( .');
    }
});
```

#### New
### Prompt -> Equivalent of JS `prompt()`
##### The API for `mscPrompt` and `mscConfirm` is same. Just the `onOk` callback of prompt receives a `value` parameter entered into the prompt.
* `mscPrompt(object)` :
```js
mscPrompt({
    title: 'Subscribe',
    subtitle: 'Enter your email to subscribe to the newsletter.',    // default: ''
    okText: 'Subscribe',      // default: OK
    cancelText: 'Cancel',   // default: Cancel
    dismissOverlay: true,   // default: false, closes dialog when clicked on overlay.
    placeholder: 'Enter your email'
    onOk: function(value) {
        mscAlert(value+ " has been subscribed to the newsletter.");
    },
    onCancel: function() {
        mscAlert('Sad face :( .');
    }
});
```

### Alert -> Equivalent of JS `alert()`
* `mscAlert(object)` :
```js
mscAlert("Hello World.");
```

### Installation
* Install via bower `bower install medium-style-confirm` or download [msc-style.css](http://bitwiser.in/medium-style-confirm/css/msc-style.css) and [msc-script.js](http://bitwiser.in/medium-style-confirm/js/msc-script.js).
* Include `msc-style.css` in html as `<link rel="stylesheet" href="msc-style.css">` just before ending `head` tag.
* Include `msc-script.js` in html as `<script src="msc-script.js">` just before ending `body` tag.
* Call the `mscConfirm()` function as shown above.

### LICENSE
#### MIT
