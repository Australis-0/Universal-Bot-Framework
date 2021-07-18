# Universal-Bot-Framework
 A universal bot framework module for working on Discord.js w/ plenty of extensions & syntactic sugar! Created for Midnight

# UNIVERSAL BOT FRAMEWORK:

## Abstract:

 The creation of a Universal Bot Framework as a Node.js module for Midnight will allow bot developers to rapidly create and deploy visual frameworks and interfaces via embeds/reactions as well as help standardise the creation of future bots and the maintenance of current ones.

 This framework will create complex, yet intuitive methods for the creation/initialization of embeds, database files, automatic backup and restoration systems, visual inputs, and more. They shall also serve as a basic extension of the JavaScript language, and should be able to parse user mentions, channels, roles, given timestamps, and should come inbuilt with a permissions API.

### Basic JS Extensions:

 `.findElement (arg0_array, arg1_content)` - Searches an array (arg0_array) for a specific element (arg1_content). Returns the index of arg1_content if found, returns false if not. Similar to .indexOf.

 `.hasElement (arg0_array, arg1_content)` - Searches an array (arg0_array) for a specific element (arg1_content). Returns true if found, returns false if not.

 `.parseColor (arg0_color, options)` - Parses a color provided as a string into a relevant array.\
 options:
  - type (String): rgb, hex, integer. Set to "rgb" by default. This is the value that parseColor returns, an array in the case of "rgb", a string in the case of "hex", and a number in the case of "integer".

 `.parseNumber (arg0_number, options)` - Parses a number into a string, complete with decimal separators.\
 options:
  - format (String): Set to "intl" by default.
  - round_to (Number): Set to undefined by default. Rounds to hundreths, thousands depending on input. Specified like so: 0.1 (tenths), 0.01 (hundreths), etc.

 `.parseString (arg0_string, options)` - Automatically parses a string into a given format. Defaults to removing all underscores and capitalising the first letter of each new word.\
 options:
  - capitalise_words (Boolean): Set to true by default.
  - delimiter (String): Set to "_" by default.

 `.randomElement (arg0_array, arg1_min, arg2_max)` - Returns a random element of a provided array between the first and last elements of the array unless arg1_min and arg2_max arguments are provided.

 `.randomNumber (arg0_min, arg1_max, options)` - Generates a random integer/number between arg0_min and arg1_max.\
 options:
  - type (String): integer, number. Set to "integer" by default.

 ### Basic Discord.js Extensions:

 `.initialiseDatabase (options)` - Initialises a database in addition to an Automatic Backup and Restoration System (ABRS) for short. "options" is not a required argument, but only "database.js" will ever be initialized in that case. It will also return a single variable object - the main JSON object, meaning that it should be used like so: `var main = $.initialiseDatabase();`.\
 options:
  - backup_folder (String): Set to undefined by default. Determines the dedicated folder in which backups will be read/saved.
  - max_backups (Number): Set to undefined by default. This means that unlimited backups will be kept at all times unless a proper argument is passed.
  - name (String): set to "database.js" by default.
  - save_at_interval (Number): Set to undefined by default. Determines how often data will be written to database.

 `.parseCommandLine (arg0_input)` - Returns parsed argument array with quotes accepted.
 
 #### Interface Methods [WIP]:

 #### Extended methods:
 `.channel.sendEmbed (options)` - Either takes options as a simple string, or as a complex argument, and prints an embed using it.\
 options:
  - author (String): Set to undefined by default.
  - author_icon (String): Set to undefined by default. Functions as a thumbnail for the author if author is provided.
  - author_url (String): Set to undefined by default. Functions as an author link if author is provided.
  - colour (String/Array): Either takes RGB values as array, or RGB/hex values as string.
  - description (String): Set to options as a string by default if more complex arguments are not provided.
  - fields (Object Array): Set to undefined by default. Functions as the `fields` argument.
  - fixed_width (Boolean): Set to true by default. Overriden if image value is provided.
  - footer (String): Set to undefined by default.
  - footer_icon (String): Functions as an icon for the footer. Set to undefined by default.
  - image (String): Attaches an image as a URL to the embed. Set to undefined by default.
  - title (String): Set to undefined by default.
  - timestamp (String): Attempts to convert any datestring into a valid timestamp format. Set to undefined by default.

 `.channel.sendSplitEmbed (options)` - Splits an array into an array of multiple embed objects.\
 options:
  - author (Array/String): Set to undefined by default. The author name that should be passed to each split embed.
  - author_icon (Array/String): Set to undefined by default. The author icon URL that should be passed to each split embed.
  - author_url (Array/String): Set to undefined by default. The author URL that should be passed to each split embed.
  - display_pages (Boolean): Set to false by default.
  - fields (Array of Object Arrays/Object Array): Set to undefined by default. Passes fields argument to each split embed.
  - fixed_width (Boolean): Set to true by default. Overriden if image value is provided.
  - footer (Array/String): Set to undefined by default. The footer that will be set underneath all split embeds.
  - image (Array/String): Set to undefined by default. The main image that will be displayed beneath all generated split embeds.
  - set_timestamp (Boolean): Set to false by default. Will display the timestamp along with the footer if a proper argument is passed.
  - max_characters (Number): Set to undefined by default. Overrides max_length, splits lines dynamically to prevent overflow.
  - max_length (Number): Set to 20 by default. Determines how many lines of text should display on each page.
  - title (Array/String): Set to undefined by default. The main title that will be displayed above all generated split embeds.
  - thumbnail (Array/String): Set to undefined by default. The main thumbnail that will be displayed with all generated split embeds.
