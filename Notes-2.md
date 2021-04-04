##### Videos 1 and 2
1. Syntax of IF command: IF(condition, value_if_true, value_if_false)
2. Example: =IF(C2="Critical", "***", "*")
3. Similarly, for numbers: =IF(F2>1000, 1, 0)
##### Video 3
4. IF command can also be nested. Example: =IF(C2="Critical", "***", IF(C2="High","**","*"))
##### Video 4
5. Optional args are enclosed in square brackets
6. Lookup tables are dictionaries, with key value pairs used for translation
7. To replicate the above with a lookup table, write down the values and star ratings in two columns in ascending order. Then go to data > sort and sort the columns.
8. Next, use the VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])
   - Lookup value is the ordinal value to lookup for
   - table array is the lookup table
   - Col index number is the column number for translated values in the lookup table
   - range lookup is a boolean. True allows pattern/approximate matching, False is for exact matching
   
   - Ex: VLOOKUP(C2, $E$6:$F$10, 2, FALSE)
```
   | E                | F
----------------------------
6  | Critical         | ***
-----------------------
7  | High             | **
-----------------------
8  | Low              | *
-----------------------
9  | Medium           | *
-----------------------
10 | Not Specified    | *

```
##### Video 5
8. Approximate matching can be used for numeric cases i.e Translate every number in range 20-29 to 0.03
```
   | E  | F
-----------------------
6  | 1  | 0.01
-----------------------
7  | 10 | 0.02
-----------------------
8  | 20 | 0.03
-----------------------
9  | 30 | 0.04
-----------------------
10 | 40 | 0.05
```
