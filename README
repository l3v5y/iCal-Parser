## Why is this here?

To the question "Can I open source the iCal parser?", 
my boss said "I don't see why not."

So, here it is.

## How to use this

If you're out of your mind, you can add items programmatically, like this:

    <?php
        header ('Content-type: text/calendar; charset=windows-1252');
        header("Cache-Control: public");
        header("Content-Description: File Transfer");
        header("Content-Disposition: attachment; filename=cal.ics");
        require_once ('ical.class.php');
        
        $a = new iCal ();
        
        $a->addEvent (
            "Lunch with Friends",        // event name
            "It will be Vietnamese!",    // event description
            strtotime ("Thursday 12pm"), // start time
            strtotime ("Thursday 12:55") // end time
        );
        
        echo $a->toString ();
    ?>

Alternatively, you can use a MySQL database and automate stuff from there.
