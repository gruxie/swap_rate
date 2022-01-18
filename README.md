# SWAP RATE #  

Converts nominal survey data into a numerical values based on a dictionary lookup.  It allows the user to switch nominal scale data from text to values for statistical functions and plotting.  It can also be used to RECODE text values to differnt numeric values

**Notes:**

- Assumes TEXT will have a numeric equivalent in the supplied DICT; else it will throw an unhandled exception 
- Assumes that "rateDict" is a "default" ratings dictionary that exists in memory.
- Required:  source_nom_data; the array of TEXT data you intend to convert e.g. df.[columnNameWithText]
- Optional:  listname:  the dictionary that maps the text to it's respective values; currently defaluts to RateBackDict which was used as the 5 point Likert-like scale for satisfaction.
- OUTPUT is a list that is in memory; you are on your own to assign it to a var e.g. foo=rateback(nom,dict)


def swap_rate (source_nom_data, listname=rateDict):  # source_nom is the text array, listname is the reference dict
    newList=list()  # creates an empty, temporary list for the function
    for nomRating in source_nom_data:  # nomrating is the term use for the source text that will be converted
       newList.append(listname[nomRating])  # handles the lookup and appends it to the temporary list
    return newList
    print(newList) # if not coverted to a variable, the function should print the list to stdout

- Assumes TEXT will have a numeric equivalent in the supplied DICT; else it will throw an unhandled exception 
- Assumes that the dictionary provided IS the right shchema for your levels of measurement.
- Assumes that "rateDict" is a "default" ratings dictionary that exists in memory.
- Required:  source_nom_data; the array of TEXT data you intend to convert e.g. df.[columnNameWithText]
- Optional:  listname:  the dictionary that maps the text to it's respective values; currently defaluts to RateBackDict
- which was used as the 5 point Likert-like scale for satisfaction.
- OUTPUT is a list that is in memory; you are on your own to assign it to a var e.g. foo=rateback(nom,dict)
