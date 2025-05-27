## 36122 Information Aggregator Project Documentation

Project codebase is composed of two parts: module.ipynb and client.ipynb

### 1. module.ipynb

dependencies include numpy,newsapi,bs4,requests,re,matplotlib,tkinter,IPython and unittest
newsapi require individual api key. The following non-paid key is used:
	6adfdd5a094c46daa53ea3bbb74379a5

functions:
- **headlines** - retrieve headline news from newsapi interface
- **source_id_matcher** - match news source with its corresponding news id in newsapi interface
- **info_matcher** - find each missing information in articles retrieved from newsapi by scalping its original webpage 
- **source_category_matcher** - match news source with its corresponding news category in newsapi source index
- **content_scalper** - find, clean and present full passage of each article using webscalper 
- **get_news** - function to allow user to get trendy news with a given number less than 100(maximum for free api key)

class:
- **Article** - designed to combine article information from newsapi and webscalpers and store them in class format; contains additional methods to print and display the article
- **Topnews** - GUI class designed to get and display news about keywords entered by the user. It also contains get_news feature to choose amount of articles found in the database.


### 2. client.ipynb

client program uses functions and classes from module file to complete tasks defined in the 36122 assignment introduction file. Specific sections are marked in the file. 
The program could run non-sequentially as all functionalities are imported from module file. 

The screenshot image in the GUI section must be in the same directory with client file in order to display it correctly.

class:
- **Info_matcher_TestCase** - unittest subclass designed to test the error-handling aspect of the info_matcher function in module file
- **Headlines_TestCase** - unittest subclass designed to test how the function headlines behave under different inputs. 

