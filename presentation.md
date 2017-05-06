<style>
.reveal li {
  font-size: 120%;
}

.reveal li {
  list-style-type: none;
  line-height: 1.1;
  margin-bottom: 1.5rem;
}

.reveal pre {
  border: none;
  background-color: black;
  padding: 1rem;
}

.reveal .narrow {
  width: 640px;
}

.reveal .mt {
  margin-top: 2.5rem;
}

.reveal .mb0 {
  margin-bottom: 0;
}

.reveal .mt0 {
  margin-top: 0;
}

.reveal .q {
  font-size: 130%;
}
</style>

### TensorFlow visualization with Guild AI

TensorBeat, Sunnyvale<br>May 7, 2017

[Garrett Smith](http://gar1t.com) / [@gar1t](https://twitter.com/gar1t)

<a href="https://guild.ai">
<img src="img/logo-white-lg.png" width="240" style="margin-top:3rem">
</a>

---

<section data-background="#336">
<h2>Introduction</h2>
</section>

---

## Topics

<ul>
<li class="fragment">A quick demo
<li class="fragment">Project motivation
<li class="fragment">Deeper dive
<li class="fragment">Common questions
<li class="fragment">Road map
<li class="fragment">Getting involved
</ul>

---

<section data-background="#336">
<h2>A quick demo</h2>
</section>

---

<section data-background="#336">
<h2>Project motivation</h2>
</section>

---

<ul>
<li>Streamline TensorFlow work flow, without taking over
<li class="fragment">Simplify model development, especially for new users
<li class="fragment">Encourage model reuse and collaboration
</ul>

---

## Streamline TensorFlow work flow

<pre class="fragment narrow">
$ prepare
</pre>

<pre class="fragment narrow mt">
$ train <span class="fragment">[MODEL]</span> <span class="fragment">[--profile PROFILE]</span>
</pre>

<pre class="fragment narrow mt">
$ evaluate --latest-run
</pre>

---

<pre class="narrow">
$ guild view
</pre>

<img class="fragment narrow" src="img/view-5.png">

---

<pre class="narrow">
$ guild view
</pre>

<img src="img/view-2.png" height="500">

---

<pre class="narrow">
$ guild view
</pre>

<img class="narrow" src="img/view-10.png">

---

<pre class="narrow">
$ guild serve ./runs/20170430T190348Z-expert
</pre>

<pre class="narrow fragment mt mb0">
$ curl http://localhost:6444 -d@request.json
</pre>

<pre class="narrow fragment mt0" style="font-size:18px">
[
  {
    "prediction": [
      -7.542473793029785,
      -10.782925605773926,
      -8.505668640136719,
      8.639995574951172,
      -7.128697872161865,
      17.12053108215332,
      -9.917960166931152,
      2.7283005714416504,
      -1.4990053176879883,
      8.320530891418457
    ]
  }
]
</pre>

---

## Work flow

- Develop model / training script
- Train model
- Evaluate results + repeat
- Serve model

---

## The temptation to take over

---

<ul>
<li>Canonical TensorFlow code above all else
<li class="fragment">Separate code and presentation
<li class="fragment">Maintain standard interfaces
</ul>

---

## Simplify user experience

---

<ul>
<li>Start with what's most important
<li class="fragment">Highlight model characteristics
<li class="fragment">Low level details (power features) follow
</ul>

---

<section data-background="#336">
<h2>Deeper dive</h2>
</section>

---

<section data-background="#336">
<h2>Common questions</h2>
</section>

---

<div class="q">Why another TensorBoard?</div>

---

<div class="q">Why not Jupyter notebooks?</div>

---

<div class="q">Our typical training takes several days. Do we really
need &ldquo;real time&rdquo; status updates?</div>

---

<section data-background="#336">
<h2>Road map</h2>
</section>

---

<ul>
<li>Enhanced visualization
<li class="fragment">Intelligent run analysis and comparison
<li class="fragment">Component / plugin exchange with TensorBoard project
<li class="fragment">Really great examples
<li class="fragment">Open source + open science + open results
</ul>

---

<section data-background="#336">
<h2>Getting involved</h2>
</section>

---

<ul>
<li>https://github.com/guildai/guild
<li class="fragment">Apache 2.0 license
<li class="fragment">Polymer web components
<li class="fragment">Python interface to TensorFlow
<li class="fragment">Shell and Python interface to OS
</ul>
