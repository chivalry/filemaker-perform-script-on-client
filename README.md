# Perform Script on Client

In April, 2014, Jan Stieperaere of Click Works [revealed](http://www.clickworks.be/en/trigger-script-another-client) a technique
for having one FileMaker client execute a script on another client without the need for a looping script. It's quite ingenious
and is based on the fact that if a client is viewing a record on a layout with an OnRecordLoad script trigger, and another
client deletes that record, the script trigger will fire.

This FileMaker module is going to hopefully allow the easy integration of this technique into existing FileMaker solutions. It
will be generally organized around the [Modular FileMaker](http://www.modularfilemaker.org/documentation/) standards, but with
one major exception (which is why at this point you won't find it listed there for the time being). I don't agree that custom
functions should by default be avoided. In fact, [quite the
opposite](http://chivalrysoftware.com/index.php/blog/131-glorious-custom-functions). I feel that if some code can be
encapsulated in a custom function, then it probably should.

With that in mind, certain domains of my [custom function library](https://github.com/chivalry/filemaker-custom-functions) will be required. The required functions will be included in the module file or the integrator can import the entire master library.

Jan did a wonderful job of creating a [WebDirect PDF module](http://www.modularfilemaker.org/module/pdf-in-webdirect/), but I'm
looking to build a more general module that allows more general message sending from one client to another. Therefore, the goals
of this module are as follows:

- Provide a complete Perform Script on Client mechanism
- Allow the integrator to either use the session and message tables included in the module or specify existing tables
- ...
