# jQueryCustom

Customized jQuery versions that namespace jQuery as jQueryCustom.  Good for including in places where jQuery is already there and you need a different version.

## Usage

```
  <!-- Original version of jQuery -->
  <script src="http://code.jquery.com/jquery-1.7.1.min.js"></script>
  
  <!-- jQueryCustom (comes in noConflict mode) -->
  <script src="./jquery-1.7.2.custom.min.js"></script>
  
  <!-- Testing -->
  <script type="text/javascript">
    // Original jQuery
    $('.orig-jquery').html('Orig jQuery version: ' + $.fn.jquery);
  
    // jQueryCustom
    (function($, window, undefined) {
      $('.custom-jquery').html('Custom jQuery version: ' + $.fn.jquery);
    })(jQueryCustom, window)
  </script>
```