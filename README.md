<h1 class="code-line" data-line-start=0 data-line-end=1 ><a id="MongoDB_0"></a>MongoDB</h1>
<p class="has-line-data" data-line-start="3" data-line-end="4">MongoDB is a document database designed for ease of development and scaling.</p>
<p class="has-line-data" data-line-start="5" data-line-end="6"><strong>The advantages of using documents are</strong>:</p>
<ul>
<li class="has-line-data" data-line-start="6" data-line-end="7">Documents (i.e. objects) correspond to native data types in many programming languages.</li>
<li class="has-line-data" data-line-start="7" data-line-end="8">Embedded documents and arrays reduce need for expensive joins.</li>
<li class="has-line-data" data-line-start="8" data-line-end="10">Dynamic schema supports fluent polymorphism.</li>
</ul>
<h3 class="code-line" data-line-start=10 data-line-end=11 ><a id="Key_Features_10"></a>Key Features!</h3>
<ul>
<li class="has-line-data" data-line-start="12" data-line-end="13">High performance.</li>
<li class="has-line-data" data-line-start="13" data-line-end="14">Rich query language.</li>
<li class="has-line-data" data-line-start="14" data-line-end="15">High availability.</li>
<li class="has-line-data" data-line-start="15" data-line-end="16">Horizontal scalability.</li>
<li class="has-line-data" data-line-start="16" data-line-end="18">Support for multiple storage engines.</li>
</ul>
<h3 class="code-line" data-line-start=18 data-line-end=19 ><a id="Installation_18"></a>Installation</h3>
<p class="has-line-data" data-line-start="20" data-line-end="21">If you are on a windows operating system, enter the following command in cmd.</p>
<pre><code class="has-line-data" data-line-start="22" data-line-end="24" class="language-python">python -m pip install pymongo
</code></pre>
<p class="has-line-data" data-line-start="25" data-line-end="26">If you use a terminnal, then,</p>
<pre><code class="has-line-data" data-line-start="27" data-line-end="29" class="language-python">sudo apt install python3-pip
</code></pre>
<p class="has-line-data" data-line-start="29" data-line-end="30">After executing, the installation shall be successful.</p>
<blockquote>
<p class="has-line-data" data-line-start="31" data-line-end="33">After importing the <code>MongoClient</code> library and creating a database, an error might show up.<br>
<code>dnspython module must be installed to use mongodb+srv:// URI</code></p>
</blockquote>
<p class="has-line-data" data-line-start="34" data-line-end="35">Install the library as,</p>
<pre><code class="has-line-data" data-line-start="36" data-line-end="38" class="language-python">pip3 install pymongo[srv]
</code></pre>
<p class="has-line-data" data-line-start="0" data-line-end="1"><em>MongoDB stores data in documents.</em></p>
<table class="table table-striped table-bordered">
<thead>
<tr>
<th>Relational Concept</th>
<th>MongoDB</th>
</tr>
</thead>
<tbody>
<tr>
<td>Database</td>
<td>Database</td>
</tr>
<tr>
<td>Tables</td>
<td>Collection</td>
</tr>
<tr>
<td>Rows</td>
<td>Documents</td>
</tr>
<tr>
<td>Index</td>
<td>Index</td>
</tr>
</tbody>
</table>
<h3 class="code-line" data-line-start=9 data-line-end=10 ><a id="Performing_basic_operations_using_PyMongo_9"></a>Performing basic operations using PyMongo</h3>
<ul>
<li class="has-line-data" data-line-start="11" data-line-end="12">
<h5 class="code-line" data-line-start=11 data-line-end=12 ><a id="Establising_a_secure_connection_11"></a>Establising a secure connection.</h5>
</li>
</ul>
<p class="has-line-data" data-line-start="12" data-line-end="13">To establish a connection to MongoDB with PyMongo you use the MongoClient class.</p>
<pre><code class="has-line-data" data-line-start="15" data-line-end="18" class="language-python">from pymongo import MongoClient
client = MongoClient('&lt;URL&gt;’)
</code></pre>
<p class="has-line-data" data-line-start="19" data-line-end="20">Create a Database, and then attach the url above in ‘&lt;URL&gt;’. This will check for the username and the password required to access the database and establish a connection to the server.</p>
<ul>
<li class="has-line-data" data-line-start="21" data-line-end="22">
<h5 class="code-line" data-line-start=21 data-line-end=22 ><a id="Adding_data_to_the_database_21"></a>Adding data to the database.</h5>
</li>
</ul>
<p class="has-line-data" data-line-start="22" data-line-end="24">A record in MongoDB is a document, which is a data structure composed of field and value pairs.<br>
Construct tuples in python to access key-value pairs.</p>
<pre><code class="has-line-data" data-line-start="26" data-line-end="34" class="language-python">kv1 = {<span class="hljs-string">"key1"</span>: value1, <span class="hljs-string">"key2"</span>: value2}
kv2 = {<span class="hljs-string">"key1"</span>: value3, <span class="hljs-string">"key2"</span>: value4}

db = client[<span class="hljs-string">"&lt;database&gt;"</span>]
collection = db[<span class="hljs-string">"&lt;database&gt;"</span>]

collection.insert_many([kv1, kv2])
</code></pre>
<ul>
<li class="has-line-data" data-line-start="35" data-line-end="36">
<h5 class="code-line" data-line-start=35 data-line-end=36 ><a id="Accessing_elements_from_database_35"></a>Accessing elements from database.</h5>
</li>
</ul>
<p class="has-line-data" data-line-start="36" data-line-end="37">Elements can be accessed by finding them all and iterating through them.</p>
<pre><code class="has-line-data" data-line-start="39" data-line-end="44" class="language-python">result = collection.find({})

<span class="hljs-keyword">for</span> i <span class="hljs-keyword">in</span> result:
    i[<span class="hljs-string">"key1"</span>]
</code></pre>
<ul>
<li class="has-line-data" data-line-start="45" data-line-end="46">
<h5 class="code-line" data-line-start=45 data-line-end=46 ><a id="Deleting_a_document_from_the_database_45"></a>Deleting a document from the database.</h5>
</li>
</ul>
<p class="has-line-data" data-line-start="46" data-line-end="47">Elements can be deleted by accessing <code>delete_many</code> method from <code>collection</code> object.</p>
<pre><code class="has-line-data" data-line-start="49" data-line-end="51" class="language-python">collection.delete_one({<span class="hljs-string">"key1"</span>: &lt;value&gt;})
</code></pre>
<p class="has-line-data" data-line-start="52" data-line-end="54">This block of code deletes the document with that key value pair.<br>
We can even delete multiple documnets at-once by specifying more arguments.</p>
<h4 class="code-line" data-line-start=55 data-line-end=56 ><a id="These_are_the_basic_operations_55"></a>These are the basic operations</h4>
<br>
<p class="has-line-data" data-line-start="57" data-line-end="59">MongoDB can be done in many laguages.<br>
See <a href="https://docs.mongodb.com/manual/">MongoDB Documentation</a></p>
