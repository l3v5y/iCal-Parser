## Why is this here?

Forked from 1337/iCal-Parser, with modifications to suit what I'm using it for

So, here it is.

## How to use this

If you're out of your mind, you can add items programmatically, like this:
```php
<?php
    // make sure Outlook knows what it is
    header('Content-type: text/calendar; charset=windows-1252');
    header('Cache-Control: public');
    header('Content-Description: File Transfer');
    header('Content-Disposition: attachment; filename=cal.ics');

    require_once('ical.class.php');

    $cal = new iCal();

    $cal->addEvent('Lunch with Friends',          // event name
                 'It will be Vietnamese!',      // event description
                 strtotime('Thursday 12pm'));  // end time
    echo $cal;
?>
```

Alternatively, you can use a MySQL database and automate stuff from there.
