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
