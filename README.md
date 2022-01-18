# SWAP RATE #  

Converts nominal survey data into a numerical values based on a dictionary lookup.  It allows the user to switch nominal scale data from text to values for statistical functions and plotting.  It can also be used to RECODE text values to differnt numeric values.  The notebook in this repo demos how to use the function for both use cases.  

** Usage: **  
swap_rate(dataframe.column_with_text, dict_with_lookup_values)


**Notes:**
- Assumes TEXT will have a numeric equivalent in the supplied DICT; else it will throw an unhandled exception 
- Assumes that "rateDict" is a "default" ratings dictionary that exists in memory.
- Required:  source_nom_data; the array of TEXT data you intend to convert e.g. df.[columnNameWithText]
- Optional:  listname:  the dictionary that maps the text to it's respective values; currently defaluts to RateBackDict which was used as the 5 point Likert-like scale for satisfaction.
- OUTPUT is a list that is in memory; you are on your own to assign it to a var e.g. foo=rateback(nom,dict)
