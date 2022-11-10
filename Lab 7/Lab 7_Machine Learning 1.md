<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en"><head>

<meta charset="utf-8">
<meta name="generator" content="quarto-1.1.189">

<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">


<title>Lab 7</title>
<style>
code{white-space: pre-wrap;}
span.smallcaps{font-variant: small-caps;}
div.columns{display: flex; gap: min(4vw, 1.5em);}
div.column{flex: auto; overflow-x: auto;}
div.hanging-indent{margin-left: 1.5em; text-indent: -1.5em;}
ul.task-list{list-style: none;}
ul.task-list li input[type="checkbox"] {
  width: 0.8em;
  margin: 0 0.8em 0.2em -1.6em;
  vertical-align: middle;
}
pre > code.sourceCode { white-space: pre; position: relative; }
pre > code.sourceCode > span { display: inline-block; line-height: 1.25; }
pre > code.sourceCode > span:empty { height: 1.2em; }
.sourceCode { overflow: visible; }
code.sourceCode > span { color: inherit; text-decoration: inherit; }
div.sourceCode { margin: 1em 0; }
pre.sourceCode { margin: 0; }
@media screen {
div.sourceCode { overflow: auto; }
}
@media print {
pre > code.sourceCode { white-space: pre-wrap; }
pre > code.sourceCode > span { text-indent: -5em; padding-left: 5em; }
}
pre.numberSource code
  { counter-reset: source-line 0; }
pre.numberSource code > span
  { position: relative; left: -4em; counter-increment: source-line; }
pre.numberSource code > span > a:first-child::before
  { content: counter(source-line);
    position: relative; left: -1em; text-align: right; vertical-align: baseline;
    border: none; display: inline-block;
    -webkit-touch-callout: none; -webkit-user-select: none;
    -khtml-user-select: none; -moz-user-select: none;
    -ms-user-select: none; user-select: none;
    padding: 0 4px; width: 4em;
    color: #aaaaaa;
  }
pre.numberSource { margin-left: 3em; border-left: 1px solid #aaaaaa;  padding-left: 4px; }
div.sourceCode
  {   }
@media screen {
pre > code.sourceCode > span > a:first-child::before { text-decoration: underline; }
}
code span.al { color: #ff0000; font-weight: bold; } /* Alert */
code span.an { color: #60a0b0; font-weight: bold; font-style: italic; } /* Annotation */
code span.at { color: #7d9029; } /* Attribute */
code span.bn { color: #40a070; } /* BaseN */
code span.bu { color: #008000; } /* BuiltIn */
code span.cf { color: #007020; font-weight: bold; } /* ControlFlow */
code span.ch { color: #4070a0; } /* Char */
code span.cn { color: #880000; } /* Constant */
code span.co { color: #60a0b0; font-style: italic; } /* Comment */
code span.cv { color: #60a0b0; font-weight: bold; font-style: italic; } /* CommentVar */
code span.do { color: #ba2121; font-style: italic; } /* Documentation */
code span.dt { color: #902000; } /* DataType */
code span.dv { color: #40a070; } /* DecVal */
code span.er { color: #ff0000; font-weight: bold; } /* Error */
code span.ex { } /* Extension */
code span.fl { color: #40a070; } /* Float */
code span.fu { color: #06287e; } /* Function */
code span.im { color: #008000; font-weight: bold; } /* Import */
code span.in { color: #60a0b0; font-weight: bold; font-style: italic; } /* Information */
code span.kw { color: #007020; font-weight: bold; } /* Keyword */
code span.op { color: #666666; } /* Operator */
code span.ot { color: #007020; } /* Other */
code span.pp { color: #bc7a00; } /* Preprocessor */
code span.sc { color: #4070a0; } /* SpecialChar */
code span.ss { color: #bb6688; } /* SpecialString */
code span.st { color: #4070a0; } /* String */
code span.va { color: #19177c; } /* Variable */
code span.vs { color: #4070a0; } /* VerbatimString */
code span.wa { color: #60a0b0; font-weight: bold; font-style: italic; } /* Warning */
</style>


<script src="Lab 7_Machine Learning 1_files/libs/clipboard/clipboard.min.js"></script>
<script src="Lab 7_Machine Learning 1_files/libs/quarto-html/quarto.js"></script>
<script src="Lab 7_Machine Learning 1_files/libs/quarto-html/popper.min.js"></script>
<script src="Lab 7_Machine Learning 1_files/libs/quarto-html/tippy.umd.min.js"></script>
<script src="Lab 7_Machine Learning 1_files/libs/quarto-html/anchor.min.js"></script>
<link href="Lab 7_Machine Learning 1_files/libs/quarto-html/tippy.css" rel="stylesheet">
<link href="Lab 7_Machine Learning 1_files/libs/quarto-html/quarto-syntax-highlighting.css" rel="stylesheet" id="quarto-text-highlighting-styles">
<script src="Lab 7_Machine Learning 1_files/libs/bootstrap/bootstrap.min.js"></script>
<link href="Lab 7_Machine Learning 1_files/libs/bootstrap/bootstrap-icons.css" rel="stylesheet">
<link href="Lab 7_Machine Learning 1_files/libs/bootstrap/bootstrap.min.css" rel="stylesheet" id="quarto-bootstrap" data-mode="light">


</head>

<body class="fullcontent">

<div id="quarto-content" class="page-columns page-rows-contents page-layout-article">

<main class="content" id="quarto-document-content">

<header id="title-block-header" class="quarto-title-block default">
<div class="quarto-title">
<h1 class="title">Lab 7</h1>
</div>



<div class="quarto-title-meta">

    
    
  </div>
  

</header>

<section id="k-means-clustering" class="level1">
<h1>K-means Clustering</h1>
<p>Let’s make up some data to cluster.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb1"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb1-1"><a href="#cb1-1" aria-hidden="true" tabindex="-1"></a>tmp <span class="ot">&lt;-</span> <span class="fu">c</span>(<span class="fu">rnorm</span> (<span class="dv">30</span>, <span class="sc">-</span><span class="dv">3</span>), <span class="fu">rnorm</span>(<span class="dv">30</span>,<span class="dv">3</span>))</span>
<span id="cb1-2"><a href="#cb1-2" aria-hidden="true" tabindex="-1"></a>x <span class="ot">&lt;-</span> <span class="fu">cbind</span>(<span class="at">x=</span> tmp, <span class="at">y=</span> <span class="fu">rev</span>(tmp))</span>
<span id="cb1-3"><a href="#cb1-3" aria-hidden="true" tabindex="-1"></a><span class="fu">plot</span>(x)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-7_Machine-Learning-1_files/figure-html/unnamed-chunk-1-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<p>The function to do k-means clustering in base R is called ‘kmeans()’.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb2"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb2-1"><a href="#cb2-1" aria-hidden="true" tabindex="-1"></a><span class="fu">kmeans</span>(x, <span class="at">centers=</span><span class="dv">2</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>K-means clustering with 2 clusters of sizes 30, 30

Cluster means:
          x         y
1 -3.116456  3.106900
2  3.106900 -3.116456

Clustering vector:
 [1] 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 2 2 2 2 2 2 2 2
[39] 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2

Within cluster sum of squares by cluster:
[1] 48.71496 48.71496
 (between_SS / total_SS =  92.3 %)

Available components:

[1] "cluster"      "centers"      "totss"        "withinss"     "tot.withinss"
[6] "betweenss"    "size"         "iter"         "ifault"      </code></pre>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb4"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb4-1"><a href="#cb4-1" aria-hidden="true" tabindex="-1"></a>km <span class="ot">&lt;-</span> <span class="fu">kmeans</span>(x, <span class="at">centers =</span> <span class="dv">4</span>, <span class="at">nstart=</span><span class="dv">20</span>)</span>
<span id="cb4-2"><a href="#cb4-2" aria-hidden="true" tabindex="-1"></a>km</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>K-means clustering with 4 clusters of sizes 27, 20, 10, 3

Cluster means:
          x          y
1  3.183322 -3.3760253
2 -3.637282  3.3385962
3 -2.074805  2.6435086
4  2.419101 -0.7803352

Clustering vector:
 [1] 2 3 2 2 2 3 2 2 3 2 3 2 3 2 2 3 3 2 3 2 2 2 3 2 2 2 3 2 2 2 1 1 1 4 1 1 1 1
[39] 1 1 1 4 1 1 1 1 1 1 1 4 1 1 1 1 1 1 1 1 1 1

Within cluster sum of squares by cluster:
[1] 27.480716 17.713600 11.504831  1.465811
 (between_SS / total_SS =  95.4 %)

Available components:

[1] "cluster"      "centers"      "totss"        "withinss"     "tot.withinss"
[6] "betweenss"    "size"         "iter"         "ifault"      </code></pre>
</div>
</div>
<p>##Q. What ‘component’ of your results object details - cluster size - cluster assignment/membership - cluster center</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb6"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb6-1"><a href="#cb6-1" aria-hidden="true" tabindex="-1"></a><span class="co">#will provide cluster size</span></span>
<span id="cb6-2"><a href="#cb6-2" aria-hidden="true" tabindex="-1"></a>km<span class="sc">$</span>size</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 27 20 10  3</code></pre>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb8"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb8-1"><a href="#cb8-1" aria-hidden="true" tabindex="-1"></a><span class="co">#will provide cluster center</span></span>
<span id="cb8-2"><a href="#cb8-2" aria-hidden="true" tabindex="-1"></a>km<span class="sc">$</span>center</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>          x          y
1  3.183322 -3.3760253
2 -3.637282  3.3385962
3 -2.074805  2.6435086
4  2.419101 -0.7803352</code></pre>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb10"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb10-1"><a href="#cb10-1" aria-hidden="true" tabindex="-1"></a><span class="co">#Membership vector</span></span>
<span id="cb10-2"><a href="#cb10-2" aria-hidden="true" tabindex="-1"></a>km<span class="sc">$</span>cluster</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code> [1] 2 3 2 2 2 3 2 2 3 2 3 2 3 2 2 3 3 2 3 2 2 2 3 2 2 2 3 2 2 2 1 1 1 4 1 1 1 1
[39] 1 1 1 4 1 1 1 1 1 1 1 4 1 1 1 1 1 1 1 1 1 1</code></pre>
</div>
</div>
<p>##Q. Plot x colored by the kmeans cluster assignment and add cluster centers as blue points</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb12"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb12-1"><a href="#cb12-1" aria-hidden="true" tabindex="-1"></a><span class="fu">plot</span>(x, <span class="at">col=</span>km<span class="sc">$</span>cluster)</span>
<span id="cb12-2"><a href="#cb12-2" aria-hidden="true" tabindex="-1"></a><span class="fu">points</span>(km<span class="sc">$</span>centers, <span class="at">col=</span><span class="st">"blue"</span>, <span class="at">pch=</span><span class="dv">15</span>, <span class="at">cex=</span><span class="fl">1.5</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-7_Machine-Learning-1_files/figure-html/unnamed-chunk-7-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<section id="hclust" class="level2">
<h2 class="anchored" data-anchor-id="hclust">hclust()</h2>
<p>Hierarchical Clustering</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb13"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb13-1"><a href="#cb13-1" aria-hidden="true" tabindex="-1"></a>hc <span class="ot">&lt;-</span> <span class="fu">hclust</span>( <span class="fu">dist</span>(x))</span>
<span id="cb13-2"><a href="#cb13-2" aria-hidden="true" tabindex="-1"></a>hc</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>
Call:
hclust(d = dist(x))

Cluster method   : complete 
Distance         : euclidean 
Number of objects: 60 </code></pre>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb15"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb15-1"><a href="#cb15-1" aria-hidden="true" tabindex="-1"></a><span class="fu">plot</span>(hc)</span>
<span id="cb15-2"><a href="#cb15-2" aria-hidden="true" tabindex="-1"></a><span class="fu">abline</span>(<span class="at">h=</span><span class="dv">8</span>, <span class="at">col=</span><span class="st">"red"</span>, <span class="at">lty=</span><span class="dv">2</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-7_Machine-Learning-1_files/figure-html/unnamed-chunk-9-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<p>To get my “main” result (cluster membership), I want to</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb16"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb16-1"><a href="#cb16-1" aria-hidden="true" tabindex="-1"></a><span class="fu">cutree</span>(hc, <span class="at">h=</span><span class="dv">8</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code> [1] 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 2 2 2 2 2 2 2 2
[39] 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2</code></pre>
</div>
</div>
<p>More often we will use ‘cutree()’ with k=2 for example</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb18"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb18-1"><a href="#cb18-1" aria-hidden="true" tabindex="-1"></a>grps <span class="ot">=</span> <span class="fu">cutree</span>(hc, <span class="at">k=</span><span class="dv">3</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<p>Make a plot of our ‘hclust()’ results i.e.&nbsp;our data colored by cluster assignment</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb19"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb19-1"><a href="#cb19-1" aria-hidden="true" tabindex="-1"></a><span class="fu">plot</span>(x, <span class="at">col=</span> grps)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-7_Machine-Learning-1_files/figure-html/unnamed-chunk-12-1.png" class="img-fluid" width="672"></p>
</div>
</div>
</section>
</section>
<section id="principal-component-analysis-pca" class="level1">
<h1>Principal Component Analysis (PCA)</h1>
<div class="cell">
<div class="sourceCode cell-code" id="cb20"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb20-1"><a href="#cb20-1" aria-hidden="true" tabindex="-1"></a>url <span class="ot">&lt;-</span> <span class="st">"https://tinyurl.com/UK-foods"</span></span>
<span id="cb20-2"><a href="#cb20-2" aria-hidden="true" tabindex="-1"></a>x <span class="ot">&lt;-</span> <span class="fu">read.csv</span>(url)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<p>##Q1. How many rows and columns are in your new data frame named x? What R functions could you use to answer this questions?</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb21"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb21-1"><a href="#cb21-1" aria-hidden="true" tabindex="-1"></a><span class="fu">nrow</span>(x)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 17</code></pre>
</div>
<div class="sourceCode cell-code" id="cb23"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb23-1"><a href="#cb23-1" aria-hidden="true" tabindex="-1"></a><span class="fu">ncol</span>(x)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 5</code></pre>
</div>
</div>
<p>There are 17 rows and 5 columns.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb25"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb25-1"><a href="#cb25-1" aria-hidden="true" tabindex="-1"></a><span class="fu">View</span>(x)</span>
<span id="cb25-2"><a href="#cb25-2" aria-hidden="true" tabindex="-1"></a><span class="fu">head</span>(x)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>               X England Wales Scotland N.Ireland
1         Cheese     105   103      103        66
2  Carcass_meat      245   227      242       267
3    Other_meat      685   803      750       586
4           Fish     147   160      122        93
5 Fats_and_oils      193   235      184       209
6         Sugars     156   175      147       139</code></pre>
</div>
<div class="sourceCode cell-code" id="cb27"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb27-1"><a href="#cb27-1" aria-hidden="true" tabindex="-1"></a><span class="fu">tail</span>(x)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>                   X England Wales Scotland N.Ireland
12      Fresh_fruit     1102  1137      957       674
13          Cereals     1472  1582     1462      1494
14         Beverages      57    73       53        47
15      Soft_drinks     1374  1256     1572      1506
16 Alcoholic_drinks      375   475      458       135
17    Confectionery       54    64       62        41</code></pre>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb29"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb29-1"><a href="#cb29-1" aria-hidden="true" tabindex="-1"></a><span class="fu">rownames</span>(x) <span class="ot">&lt;-</span> x[,<span class="dv">1</span>]</span>
<span id="cb29-2"><a href="#cb29-2" aria-hidden="true" tabindex="-1"></a>x <span class="ot">&lt;-</span> x[,<span class="sc">-</span><span class="dv">1</span>]</span>
<span id="cb29-3"><a href="#cb29-3" aria-hidden="true" tabindex="-1"></a><span class="fu">head</span>(x)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>               England Wales Scotland N.Ireland
Cheese             105   103      103        66
Carcass_meat       245   227      242       267
Other_meat         685   803      750       586
Fish               147   160      122        93
Fats_and_oils      193   235      184       209
Sugars             156   175      147       139</code></pre>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb31"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb31-1"><a href="#cb31-1" aria-hidden="true" tabindex="-1"></a><span class="fu">dim</span>(x)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 17  4</code></pre>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb33"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb33-1"><a href="#cb33-1" aria-hidden="true" tabindex="-1"></a>x <span class="ot">&lt;-</span> <span class="fu">read.csv</span>(url, <span class="at">row.names=</span><span class="dv">1</span>)</span>
<span id="cb33-2"><a href="#cb33-2" aria-hidden="true" tabindex="-1"></a><span class="fu">head</span>(x)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>               England Wales Scotland N.Ireland
Cheese             105   103      103        66
Carcass_meat       245   227      242       267
Other_meat         685   803      750       586
Fish               147   160      122        93
Fats_and_oils      193   235      184       209
Sugars             156   175      147       139</code></pre>
</div>
</div>
<p>##Q2. Which approach to solving the ‘row-names problem’ mentioned above do you prefer and why? Is one approach more robust than another under certain circumstances?</p>
<p>The second approach (x &lt;- read.csv(url, row.names=1)) because it is a single step and easier to remember. They are both equally robust if the dataset is the same.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb35"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb35-1"><a href="#cb35-1" aria-hidden="true" tabindex="-1"></a><span class="fu">barplot</span>(<span class="fu">as.matrix</span>(x), <span class="at">beside=</span>T, <span class="at">col=</span><span class="fu">rainbow</span>(<span class="fu">nrow</span>(x)))</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-7_Machine-Learning-1_files/figure-html/unnamed-chunk-19-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<p>##Q3: Changing what optional argument in the above barplot() function results in the following plot?</p>
<p>Changing beside=TRUE to beside=FALSE will provide the following plot.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb36"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb36-1"><a href="#cb36-1" aria-hidden="true" tabindex="-1"></a><span class="co">#changing beside=TRUE to beside=FALSE will provide the following plot</span></span>
<span id="cb36-2"><a href="#cb36-2" aria-hidden="true" tabindex="-1"></a><span class="fu">barplot</span>(<span class="fu">as.matrix</span>(x), <span class="at">beside=</span><span class="cn">FALSE</span>, <span class="at">col=</span><span class="fu">rainbow</span>(<span class="fu">nrow</span>(x)))</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-7_Machine-Learning-1_files/figure-html/unnamed-chunk-20-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<p>##Q5: Generating all pairwise plots may help somewhat. Can you make sense of the following code and resulting figure? What does it mean if a given point lies on the diagonal for a given plot?</p>
<p>Yes, we are generating pairwise plots by using (pairs()) using X dataset and indicating that the colors of each datapoint will be based off the rainbow colors(multiple colors instead of one color) and the pch=16 just sets the shape of the datapoint on the plot. The resulting pairwise plots provides plots of each column of the dataset (x) against each other (countries) and the named countries in the empty boxes indicate the y-axis and x-axis of each plot. For example all the plots in the England column has England’s data as the x-axis and the plots in the England row has England’s data as the y-axis. If a given point lies on the diagonal for a given plot it means that the value is the same for the two countries (x-axis and y-axis).</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb37"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb37-1"><a href="#cb37-1" aria-hidden="true" tabindex="-1"></a><span class="fu">pairs</span>(x, <span class="at">col=</span><span class="fu">rainbow</span>(<span class="dv">10</span>), <span class="at">pch=</span><span class="dv">16</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-7_Machine-Learning-1_files/figure-html/unnamed-chunk-21-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<section id="pca-to-the-rescue" class="level2">
<h2 class="anchored" data-anchor-id="pca-to-the-rescue">PCA to the rescue!</h2>
<p>The main function in base R to do PCA is called ‘prcomp()’ One issue with the ‘prcomp()’ function is that it expects the transpose of our data as input.</p>
<p>##Q6. What is the main differences between N. Ireland and the other countries of the UK in terms of this data-set? A main difference between N. Ireland and other countries is that the data has some outliers more outliers compared to the rest.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb38"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb38-1"><a href="#cb38-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Use the prcomp() PCA function to return a list object.</span></span>
<span id="cb38-2"><a href="#cb38-2" aria-hidden="true" tabindex="-1"></a>pca <span class="ot">&lt;-</span> <span class="fu">prcomp</span>( <span class="fu">t</span>(x) )</span>
<span id="cb38-3"><a href="#cb38-3" aria-hidden="true" tabindex="-1"></a><span class="fu">summary</span>(pca)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>Importance of components:
                            PC1      PC2      PC3       PC4
Standard deviation     324.1502 212.7478 73.87622 4.189e-14
Proportion of Variance   0.6744   0.2905  0.03503 0.000e+00
Cumulative Proportion    0.6744   0.9650  1.00000 1.000e+00</code></pre>
</div>
</div>
<p>##Q7. Complete the code below to generate a plot of PC1 vs PC2. The second line adds text labels over the data points.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb40"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb40-1"><a href="#cb40-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Plot PC1 vs PC2</span></span>
<span id="cb40-2"><a href="#cb40-2" aria-hidden="true" tabindex="-1"></a><span class="fu">plot</span>(pca<span class="sc">$</span>x[,<span class="dv">1</span>], pca<span class="sc">$</span>x[,<span class="dv">2</span>], <span class="at">xlab=</span><span class="st">"PC1"</span>, <span class="at">ylab=</span><span class="st">"PC2"</span>, <span class="at">xlim=</span><span class="fu">c</span>(<span class="sc">-</span><span class="dv">270</span>,<span class="dv">500</span>))</span>
<span id="cb40-3"><a href="#cb40-3" aria-hidden="true" tabindex="-1"></a><span class="fu">text</span>(pca<span class="sc">$</span>x[,<span class="dv">1</span>], pca<span class="sc">$</span>x[,<span class="dv">2</span>], <span class="fu">colnames</span>(x))</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-7_Machine-Learning-1_files/figure-html/unnamed-chunk-23-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<p>##Q8. Customize your plot so that the colors of the country names match the colors in our UK and Ireland map and table at start of this document.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb41"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb41-1"><a href="#cb41-1" aria-hidden="true" tabindex="-1"></a><span class="fu">plot</span>(pca<span class="sc">$</span>x[,<span class="dv">1</span>], pca<span class="sc">$</span>x[,<span class="dv">2</span>], <span class="at">xlab=</span><span class="st">"PC1"</span>, <span class="at">ylab=</span><span class="st">"PC2"</span>, <span class="at">xlim=</span><span class="fu">c</span>(<span class="sc">-</span><span class="dv">270</span>,<span class="dv">500</span>))</span>
<span id="cb41-2"><a href="#cb41-2" aria-hidden="true" tabindex="-1"></a><span class="fu">text</span>(pca<span class="sc">$</span>x[,<span class="dv">1</span>], pca<span class="sc">$</span>x[,<span class="dv">2</span>], <span class="fu">colnames</span>(x), <span class="at">col=</span><span class="fu">c</span>(<span class="st">"orange"</span>, <span class="st">"red"</span>, <span class="st">"blue"</span>, <span class="st">"darkgreen"</span>))</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-7_Machine-Learning-1_files/figure-html/unnamed-chunk-24-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb42"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb42-1"><a href="#cb42-1" aria-hidden="true" tabindex="-1"></a><span class="co">#Code below: Use square of pca$sdev , which stands for “standard deviation”, to calculate how much variation in the original data each PC accounts for</span></span>
<span id="cb42-2"><a href="#cb42-2" aria-hidden="true" tabindex="-1"></a>v <span class="ot">&lt;-</span> <span class="fu">round</span>( pca<span class="sc">$</span>sdev<span class="sc">^</span><span class="dv">2</span><span class="sc">/</span><span class="fu">sum</span>(pca<span class="sc">$</span>sdev<span class="sc">^</span><span class="dv">2</span>) <span class="sc">*</span> <span class="dv">100</span> )</span>
<span id="cb42-3"><a href="#cb42-3" aria-hidden="true" tabindex="-1"></a>v</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 67 29  4  0</code></pre>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb44"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb44-1"><a href="#cb44-1" aria-hidden="true" tabindex="-1"></a><span class="co">#Alternative method to calculate how much variation in the original data</span></span>
<span id="cb44-2"><a href="#cb44-2" aria-hidden="true" tabindex="-1"></a>z <span class="ot">&lt;-</span> <span class="fu">summary</span>(pca)</span>
<span id="cb44-3"><a href="#cb44-3" aria-hidden="true" tabindex="-1"></a>z<span class="sc">$</span>importance</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>                             PC1       PC2      PC3          PC4
Standard deviation     324.15019 212.74780 73.87622 4.188568e-14
Proportion of Variance   0.67444   0.29052  0.03503 0.000000e+00
Cumulative Proportion    0.67444   0.96497  1.00000 1.000000e+00</code></pre>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb46"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb46-1"><a href="#cb46-1" aria-hidden="true" tabindex="-1"></a><span class="fu">barplot</span>(v, <span class="at">xlab=</span><span class="st">"Principal Component"</span>, <span class="at">ylab=</span><span class="st">"Percent Variation"</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-7_Machine-Learning-1_files/figure-html/unnamed-chunk-27-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb47"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb47-1"><a href="#cb47-1" aria-hidden="true" tabindex="-1"></a><span class="do">## Lets focus on PC1 as it accounts for &gt; 90% of variance </span></span>
<span id="cb47-2"><a href="#cb47-2" aria-hidden="true" tabindex="-1"></a><span class="fu">par</span>(<span class="at">mar=</span><span class="fu">c</span>(<span class="dv">10</span>, <span class="dv">3</span>, <span class="fl">0.35</span>, <span class="dv">0</span>))</span>
<span id="cb47-3"><a href="#cb47-3" aria-hidden="true" tabindex="-1"></a><span class="fu">barplot</span>( pca<span class="sc">$</span>rotation[,<span class="dv">1</span>], <span class="at">las=</span><span class="dv">2</span> )</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-7_Machine-Learning-1_files/figure-html/unnamed-chunk-28-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<p>##Q9: Generate a similar ‘loadings plot’ for PC2. What two food groups feature prominantely and what does PC2 maninly tell us about?</p>
<p>Fresh potatoes and Soft Drinks. PC2 plot is explaining how each variable is contributing/affecting PC2.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb48"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb48-1"><a href="#cb48-1" aria-hidden="true" tabindex="-1"></a><span class="fu">par</span>(<span class="at">mar=</span><span class="fu">c</span>(<span class="dv">10</span>, <span class="dv">3</span>, <span class="fl">0.35</span>, <span class="dv">0</span>))</span>
<span id="cb48-2"><a href="#cb48-2" aria-hidden="true" tabindex="-1"></a><span class="fu">barplot</span>( pca<span class="sc">$</span>rotation[,<span class="dv">2</span>], <span class="at">las=</span><span class="dv">2</span> )</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-7_Machine-Learning-1_files/figure-html/unnamed-chunk-29-1.png" class="img-fluid" width="672"></p>
</div>
</div>
</section>
</section>

</main>
<!-- /main column -->
<script id="quarto-html-after-body" type="application/javascript">
window.document.addEventListener("DOMContentLoaded", function (event) {
  const toggleBodyColorMode = (bsSheetEl) => {
    const mode = bsSheetEl.getAttribute("data-mode");
    const bodyEl = window.document.querySelector("body");
    if (mode === "dark") {
      bodyEl.classList.add("quarto-dark");
      bodyEl.classList.remove("quarto-light");
    } else {
      bodyEl.classList.add("quarto-light");
      bodyEl.classList.remove("quarto-dark");
    }
  }
  const toggleBodyColorPrimary = () => {
    const bsSheetEl = window.document.querySelector("link#quarto-bootstrap");
    if (bsSheetEl) {
      toggleBodyColorMode(bsSheetEl);
    }
  }
  toggleBodyColorPrimary();  
  const icon = "";
  const anchorJS = new window.AnchorJS();
  anchorJS.options = {
    placement: 'right',
    icon: icon
  };
  anchorJS.add('.anchored');
  const clipboard = new window.ClipboardJS('.code-copy-button', {
    target: function(trigger) {
      return trigger.previousElementSibling;
    }
  });
  clipboard.on('success', function(e) {
    // button target
    const button = e.trigger;
    // don't keep focus
    button.blur();
    // flash "checked"
    button.classList.add('code-copy-button-checked');
    var currentTitle = button.getAttribute("title");
    button.setAttribute("title", "Copied!");
    setTimeout(function() {
      button.setAttribute("title", currentTitle);
      button.classList.remove('code-copy-button-checked');
    }, 1000);
    // clear code selection
    e.clearSelection();
  });
  function tippyHover(el, contentFn) {
    const config = {
      allowHTML: true,
      content: contentFn,
      maxWidth: 500,
      delay: 100,
      arrow: false,
      appendTo: function(el) {
          return el.parentElement;
      },
      interactive: true,
      interactiveBorder: 10,
      theme: 'quarto',
      placement: 'bottom-start'
    };
    window.tippy(el, config); 
  }
  const noterefs = window.document.querySelectorAll('a[role="doc-noteref"]');
  for (var i=0; i<noterefs.length; i++) {
    const ref = noterefs[i];
    tippyHover(ref, function() {
      // use id or data attribute instead here
      let href = ref.getAttribute('data-footnote-href') || ref.getAttribute('href');
      try { href = new URL(href).hash; } catch {}
      const id = href.replace(/^#\/?/, "");
      const note = window.document.getElementById(id);
      return note.innerHTML;
    });
  }
  var bibliorefs = window.document.querySelectorAll('a[role="doc-biblioref"]');
  for (var i=0; i<bibliorefs.length; i++) {
    const ref = bibliorefs[i];
    const cites = ref.parentNode.getAttribute('data-cites').split(' ');
    tippyHover(ref, function() {
      var popup = window.document.createElement('div');
      cites.forEach(function(cite) {
        var citeDiv = window.document.createElement('div');
        citeDiv.classList.add('hanging-indent');
        citeDiv.classList.add('csl-entry');
        var biblioDiv = window.document.getElementById('ref-' + cite);
        if (biblioDiv) {
          citeDiv.innerHTML = biblioDiv.innerHTML;
        }
        popup.appendChild(citeDiv);
      });
      return popup.innerHTML;
    });
  }
});
</script>
</div> <!-- /content -->



</body></html>