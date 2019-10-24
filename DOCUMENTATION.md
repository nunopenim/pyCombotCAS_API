# pyCombotCAS_API Documentation - Text version

This is a text version of the API Documentation. In here, all the avaliable functions
are described and explained.

# CAS_QUERY_URL

This is the [Combot CAS](https://combot.org/cas) direct query URL. Any query made here
will have it's return as a json. Global variable, in case it changes or alternative
services in future use similar system.

# get_user_data(user_id)

This function takes a user_id, with int type (although string might work too, it is casted
to string anyway). It parses that user_id and requests to the CAS_QUERY_URL the info about
it. It will then parse the json file and return the userdata as a dictionary. To access the
fields, you do like a normal Python dict. It can be used directly as a function, although
in a normal application it is irrelevant.

# isbanned(userdata)

This method parses the userdata to get a boolean which represents if a user is banned or not.
Due to it's type of input, like get_user_data(), it's direct use is irrelevant. It will return
a boolean. Quick reminder, userdata is a dict.

# banchecker(user_id)

This function will take the user_id and combine the actions of both previous functions, in order
to get a practical output. Argument is user_id, which by default is an int (string works too),
and it returns a boolean. If True, user is CAS banned. If False, user has no record in Combot
or there has been an error fetching the data.

# vercheck()

Version getter, will always returns a string that specifies the current API version. It has just
informative use.

# offenses(user_id)

This method will fetch and parse the userdata to get the number of offenses of the refered user_id.
It takes as argument an int (or string) that matches a user. It then tries to get the offenses of
that user. If successful it will return a string with a number, which matches the offense number.
Otherwise it will return "None" (not the Python None object). Return type is always a string.

# timeadded(user_id)

This function fetches and parses the user_id data to get a time (in Epoch format). As with all the 
other functions, it returns a string, but not before converting it (using Python's datetime library)
in a human readable format. It will then return the time in the format of hh:mm:ss, dd-mm-yyyy. This
time is in UTC format, for international use. If it fails to get a time (because user might not be
CAS banned at all), it returns "None" (again, not the Python None object).
