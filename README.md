# tiiny-banner
remove the annoying banner with just a little bit of js


### method one

add this to your code:

```
<script>
document.addEventListener('DOMContentLoaded', function() {

    function isBanner(element) {
        return element.style.position === 'fixed' &&
               element.style.bottom === '0%' &&
               element.style.width === '100%' &&
               element.style.height === '55px' &&
               element.style.zIndex === '9999' &&
               element.querySelector('a[href="https://tiiny.host?ref=free-site"]') &&
               element.querySelector('img[src="https://tiiny.host/assets/img/ad.png"]');
    }

    const allElements = document.querySelectorAll('*');
    allElements.forEach(element => {
        if (isBanner(element)) {
            element.remove();
        }
    });

});
</script>
```

### method two

link my cool little jsdelivr cdn thing
