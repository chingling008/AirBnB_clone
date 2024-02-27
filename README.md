# AirBnB Clone

## Description

This is the first of several lite clones of the [AirBnB](https://www.airbnb.com) (online platform for rental accommodations) website. It specifies classes for __User__, __Place__, __State__, __City__, __Amenity__, and __Review__ that inherit from the __BaseModel__ class. Instances are serialized and saved to a JSON file then reloaded and deserialized back into instances. Additionally, there is a simple command line interface (CLI) or 'console' that abstracts the process used to create these instances.

## Requirements
Python 3.4.3 or later

## Usage

The console can run in two modes: *interactive* and *non-interactive*:

### Interactive mode

To run the console in *interactive* mode type:

```$ ./console.py```

This prompt will appear:

```(hbnb) ```

### Storage

Instances of classes are saved in a [JSON](https://www.json.org) string representation to the __file.json__ file at the root directory. Any modifications (additions, deletions, updates) to the objects are saved automatically to the file. The JSON file serves as a simple database that helps the data persist across sessions. 

### Tests

Testing is imperative to building any robust program therefore we have included a comprehensive testing suite using the Python [unittest module](https://docs.python.org/3.4/library/unittest.html)

To run the entire unittest suite in one go, run the following command from the root directory:

```bash
$ python3 -m unittest discover tests
............................................................
----------------------------------------------------------------------
Ran 60 tests in 0.017s

OK
```

If you want to run tests individually, an example would be:

```bash
$ python3 -m unittest tests/test_models/test_base_model.py
.....
----------------------------------------------------------------------
Ran 5 tests in 0.003s

OK
```

### Supported Commands

Name | Description | Use
-------- | ----------- |-------- |
help | Displays help information for a command | help [command]
quit | Exits/quits the program | quit
EOF | Exits the program when files are passed into the program | N/A
create | Creates a new instance of a specified class | create [class_name]
show | Prints the string representation of an instance | show [class_name] [id]
destroy | Deletes an instance | destroy [class_name] [id]
all | Prints the string representation of all instances of a class| all or all [class_name] [id]
update | Adds or modifies attributes of an instance | update [class_name] [id] [attribute] [value]

