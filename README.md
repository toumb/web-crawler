# web-crawler

A web crawler that retrieves the HTML content from webpages and stores it in a database.

The application gives three retrieval options to the user:


1. Random crawl   
   The user gives an initial url (seed) and a number of pages.
   The crawler creates a list of all the links found in first page and then chooses
   randomly which page to crawl next. This continues until the number of pages
   is reached.
  

2. Serial crawl    
   The user gives an initial url (seed) and next page format (eg. =page2).
   The crawler searches for next pages until no more pages are found.
   This function is ideal when crawiling eg. forums and only a specific post needs
   to be collected.

  
3. Breadth-first crawl   
   The user gives an initial url (seed) and the desired level to be reached.
   For every page, the crawler gets all of the links found and stores their content in
   the database. Then repeats the same procedure for each one of them, thus implementing
   a breadth-first search.
   
     
After collecting the content, the text found in these pages is extracted and is 
stored in the database.

The database is implemented with SQLite.
