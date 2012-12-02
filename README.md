Python Table Library
====================

Some of the capabilities of the library is shown below.

    from table import Table

    table = Table(
        ["1", "2", "3"] # row names,
        ["a", "b"]      # column names,
        [[1, 2],        # initial values
         [3, 4],
         [5, 6]]
    )
    
    print "Whole table:"
    print table

    print "Just a cell:"
    print table["1", "a"]

    print "A row:"
    print table["2", :]

    print "A column:"
    print table[:, "b"]

    print "A range:"
    print table["2":, :]

The library also provides basic I/O capability for simple delimited files and standard CSV files:

    table1 = readTableFromDelimited(f)
    table2 = readTableFromCSV(f)