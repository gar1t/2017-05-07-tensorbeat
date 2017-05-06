<section data-background="#336">
<h2>Common questions</h2>
</section>

---

<div class="q">Why another TensorBoard?</div>

---

<div class="q">Why not just contribute to TensorBoard?</div>

---

<div class="q">Why not a Jupyter notebook?</div>

---

<div class="q">Our typical training takes days. Do we really need
&ldquo;real time&rdquo; status updates?</div>

---

<div class="q">What is Guild&rsquo;s impact on system resources?</div>

---

### Streamline TensorFlow work flow<br><em>without taking over</em>

<ul>
<li class="fragment">TensorFlow code alway central
<li class="fragment">Separate code and presentation (concerns)
<li class="fragment">Maintain standard interfaces
</ul>

---

## RUNDIR

<pre class="mb0" style="font-size:18px">
<span class="prompt">PROJECT/runs/20170430T190348Z-expert $</span> find .
</pre>

<pre class="fragment mt0 mb0" style="font-size:18px">
./train
./train/events.out.tfevents.1493579030.omaha
./validation
./validation/events.out.tfevents.1493579037.omaha
</pre>

<pre class="fragment mt0 mb0" style="font-size:18px">
./guild.d
./guild.d/run.db
./guild.d/sources
./guild.d/sources/Guild
./guild.d/errors.log
./guild.d/meta/...
</pre>

<pre class="fragment mt0" style="font-size:18px">
./model
./model/export.index
./model/export.data-00000-of-00001
./model/checkpoint
./model/export.meta
</pre>

---

## Run DB

<pre class="fragment mb0">
<span class="prompt">PROJECT/runs/20170430T190348Z-expert $</span> sqlite3 guild.d/run.db
</pre>

<pre class="fragment mt0 mb0">
sqlite> .tables
attr        flag        output      series      series_key
</pre>

<pre class="fragment mt0 mb0">
sqlite> select * from flag;
datadir|./data
rundir|$RUNDIR
batch_size|100
epochs|10
</pre>

<pre class="fragment mt0">
sqlite> select * from series limit 3;
1276377582|1493579028364|1|
129029817|1493579028364|1|
241768802|1493579028364|1|
</pre>

---

## Work flow

<ul>
<li>Develop model / training script
<li>Train model
<li>Evaluate results + repeat
<li>Serve model
</ul>
