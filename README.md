Modifications to code found at:
http://au.mathworks.com/matlabcentral/fileexchange/20565-json-parser

In MATLAB (R2015b), field names in a structure can only contain alphanumeric characters and underscores. This is a problem when you wish for field names to be Youtube video ID's, as they can contain dashes. Also, field names must begin with a letter, while Youtube ID's frequently do not.

My modifications cause all field names to be prepended with 'Y_', and all dashes to be replaces with underscores. This must be factored into further use of the structure generated.

## Original Description:

"This function parses JSON strings. It converts JSON arrays into cell arrays and JSON objects into structures.

This can be used with webervices that return JSON data such as the API provided by Google®.

An example of use is: 
  google_search = 'http://ajax.googleapis.com/ajax/services/search/web?v=1.0&q=matlab'; 
  matlab_results = parse_json(urlread(google_search)); 
  disp(matlab_results{1}.responseData.results{1}.titleNoFormatting) 
  disp(matlab_results{1}.responseData.results{1}.visibleUrl)"
