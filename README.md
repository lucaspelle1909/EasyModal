# How to use EasyModal

## Clone this repository
```
git clone https://github.com/wesleylopex/EasyModal.git
```

## Import CSS file

```HTML
<link rel="stylesheet" href="path/to/EasyModal.css">
```

## Add HTML

```HTML
<div class="my-easy-modal easy-modal">
  <div class="easy-modal__content">
    <h1>
      This is your customizable EasyModal body
    </h1>
    <button class="close-my-easy-modal">
      Close EasyModal
    </button>
  </div>
</div>
```

## Import JS file and create Class

```HTML
<script type="module">
  import EasyModal from 'path/to/EasyModal.js'

  const myEasyModal = new EasyModal({
    el: '.my-easy-modal',
    persistent: true,
    open: '.open-my-easy-modal',
    close: '.close-my-easy-modal',
    beforeOpen: () => console.log('before open'),
    beforeClose: () => console.log('before close')
  })

  myEasyModal.start()
</script>
```

## Options
|Attribute|Required|Default|Description|
|-|-|-|-|
|el|true|null|Selector to find your EasyModal|
|el|true|null|Selector to find your EasyModal|
|persistent|false|false|If true, modal won't close on click outrsie|
|open|false|null|Element to click and open modal|
|close|false|null|Element to click and close modal|
|beforeOpen|false|null|Function to run before modal opens|
|beforeClose|false|null|Function to run before modal closes|

## Available functions
|Function|Description|
|-|-|
|start()|Start EasyModal class. If not used, EasyModal won't work
|open()|Opens the modal
|close()|Closes the modal

