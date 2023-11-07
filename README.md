# nandgame
my Nandgame solutions

## File formatting
All solutions are in separate JSON files with the following structures

### Structures

file:
{
    "name" : name,
    "parts" : \[parts\],
    "wires" : \[wires\]
}
File name is always identical to the name of the part, e.g. nand.json - {"name" : "nand", ...} - NAND gate.

    parts:
    {
        "name" : name,
        "inputs" : \[inputs\],
        "outputs" : \[outputs\]
    }
    'parts' represents basically the same object as file

        inputs:
        - array of strings with input names, e.g. "a", "b"

        outputs:
        - array of string with output names, e.g. "q", "not q"
    
    wires:
    {
        "part_s" : name_of_starting_part,
        "IO_s" : name_of_starting_IO,
        "part_e" : name_of_ending_part,
        "IO_e" : name_of_ending_IO
    }

### Special parts
There are 2 special parts in every file: INPUT, OUTPUT representing the input and output variables.

### Parts with one input/output
The input/output is named "DEF_I"/"DEF_O".

## Custom parts
Custom parts' names are of the format "\<name\>".
