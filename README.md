# Universal-Bot-Framework
 A universal bot framework module for working on Discord.js w/ plenty of extensions & syntactic sugar! Created for Midnight

# UNIVERSAL BOT FRAMEWORK:

## Abstract:

 The creation of a Universal Bot Framework as a Node.js module for Midnight will allow bot developers to rapidly create and deploy visual frameworks and interfaces via embeds/reactions as well as help standardise the creation of future bots and the maintenance of current ones.

 This framework will create complex, yet intuitive methods for the creation/initialization of embeds, database files, automatic backup and restoration systems, visual inputs, and more. They shall also serve as a basic extension of the JavaScript language, and should be able to parse user mentions, channels, roles, given timestamps, and should come inbuilt with a permissions API.

### Basic JS Extensions:

 `.findElement (arg0_array, arg1_content)` - Searches an array (arg0_array) for a specific element (arg1_content). Returns the index of arg1_content if found, returns false if not. Similar to .indexOf.

 `.hasElement (arg0_array, arg1_content)` - Searches an array (arg0_array) for a specific element (arg1_content). Returns true if found, returns false if not.

 `.parseNumber (arg0_number, options)` - Parses a number into a string, complete with decimal separators.
 options:
 format (String): Set to ‘intl’ by default.
 round_to (Number): Set to undefined by default. Rounds to hundreths, thousands depending on input. Specified like so: 0.1 (tenths), 0.01 (hundreths), etc.

 `.parseString (arg0_string, options)` - Automatically parses a string into a given format. Defaults to removing all underscores and capitalising the first letter of each new word.
 options:
 capitalise_words (Boolean): Set to true by default.
 delimiter (String): Set to ‘_’ by default.

` .randomElement (arg0_array, arg1_min, arg2_max)` - Returns a random element of a provided array between the first and last elements of the array unless arg1_min and arg2_max arguments are provided.

 `.randomNumber (arg0_min, arg1_max, options)` - Generates a random integer/number between arg0_min and arg1_max.
 options:
 type (String): integer, number. Set to ‘integer’ by default.

 ### Basic Discord.js Extensions:

` .parseCommandLine (arg0_input)` - Returns parsed argument array with quotes accepted.
