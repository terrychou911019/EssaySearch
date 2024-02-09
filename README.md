# Essay Search
A simple search engine with different search methods.

## Description
Given a word, the search engine will list the essays whose titles or abstracts contain that word. Note that this program only considers alphabetic words, so special symbols or digits will be ignored. Queries are also case insensitive. 

This program provides some search methods:
- exact search
- prefix search
- suffix search
- and operator
- or operator

In this program, we consider the first line of the essay as the title.

## Getting Started
### Dependencies
- Windows

### Packages
- data - example data
- data-more - more example data
- query
    - query-results.txt - example query results
    - query.txt - example query
- query-more
    - query-more-results.txt - more example query results
    - query-more.txt - more example query
- main.cpp - essay search engine

### Installing
```bash
git clone https://github.com/terrychou911019/EssaySearch.git
```

### Executing Program
__Input__
- #### Essay file
    There are a set of essay txt files, and these essay txt files will be put in the given directory.
    Every essay txt files contains two parts:
    - title - the first line of the essay
    - abstract - the remaining sentences
- #### Query file
    Each line represents one query that has to be processed, and there can be several queries in a query file. Note that the _"and operator"_ and _"or operator"_ are left associative.
    Here are some search methods you can use:
    - exact search - "search-word"
    - prefix search - search-word
    - suffix search - \*search-word\*
    - and operator - "+"
    - or operator - "/"
    
    Here are some query examples:
    - __reflect__ - find essays that have word with _prefix "reflect"_, eg: reflect, reflection.
    - __“graph” / \*composition\*__ - find essays that have _exactly_ the word _"graph"_ or the essays that have words with _suffix "composition"_
    - __“graph” + decompos__ - find essays that have _exactly_ the word _"graph"_ and the essays that have words with _prefix "decompos"_

    Note that upper-case and lower-case characters are treated the same.

__Output__
- When executing your program, the output file name is provided as an argument. 
- Output the essay titles of the search results in the output file. 
- Each essay title should be followed by a new line character. If not found, print out _"Not Found!"_
- The output order follows the order of the essays.

__Execute__
1. Compile main.cpp, it will generate a file named "main.exe".
    ```bash
    g++ main.cpp -o main.exe
    ```
2. Execute the program.
    ```bash
    ./main.exe <data folder path> <query file path> <output file name>
    ```
    Here is an example:
    ```bash
    ./main.exe ./data ./query/query.txt ./output.txt
    ```
    In this example, it will generate a file named _"output.txt"_ containing the results of the essay search.

### Help 
- We only consider alphabetic words.
- Queries are case insensitive.
- We consider the first line of the essay as the title.
