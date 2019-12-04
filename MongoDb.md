# MongoDB


MongoDB is a document database designed for ease of development and scaling.

__The advantages of using documents are__:
  - Documents (i.e. objects) correspond to native data types in many programming languages.
  - Embedded documents and arrays reduce need for expensive joins.
  - Dynamic schema supports fluent polymorphism.

### Key Features!

  - High performance.
  - Rich query language.
  - High availability.
  - Horizontal scalability.
  - Support for multiple storage engines.

### Installation

If you are on a windows operating system, enter the following command in cmd.
```python
python -m pip install pymongo
```

If you use a terminnal, then,
```python
sudo apt install python3-pip
```
After executing, the installation shall be successful.

>After importing the `MongoClient` library and creating a database, an error might show up. 
`dnspython module must be installed to use mongodb+srv:// URI`

Install the library as,
```python
pip3 install pymongo[srv]
```