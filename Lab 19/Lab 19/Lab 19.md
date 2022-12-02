<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en"><head>

<meta charset="utf-8">
<meta name="generator" content="quarto-1.1.189">

<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">

<meta name="author" content="Karen Guerrero">

<title>Lab 19</title>
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


<script src="Lab 19_files/libs/clipboard/clipboard.min.js"></script>
<script src="Lab 19_files/libs/quarto-html/quarto.js"></script>
<script src="Lab 19_files/libs/quarto-html/popper.min.js"></script>
<script src="Lab 19_files/libs/quarto-html/tippy.umd.min.js"></script>
<script src="Lab 19_files/libs/quarto-html/anchor.min.js"></script>
<link href="Lab 19_files/libs/quarto-html/tippy.css" rel="stylesheet">
<link href="Lab 19_files/libs/quarto-html/quarto-syntax-highlighting.css" rel="stylesheet" id="quarto-text-highlighting-styles">
<script src="Lab 19_files/libs/bootstrap/bootstrap.min.js"></script>
<link href="Lab 19_files/libs/bootstrap/bootstrap-icons.css" rel="stylesheet">
<link href="Lab 19_files/libs/bootstrap/bootstrap.min.css" rel="stylesheet" id="quarto-bootstrap" data-mode="light">


</head>

<body class="fullcontent">

<div id="quarto-content" class="page-columns page-rows-contents page-layout-article">

<main class="content" id="quarto-document-content">

<header id="title-block-header" class="quarto-title-block default">
<div class="quarto-title">
<h1 class="title">Lab 19</h1>
</div>



<div class="quarto-title-meta">

    <div>
    <div class="quarto-title-meta-heading">Author</div>
    <div class="quarto-title-meta-contents">
             <p>Karen Guerrero </p>
          </div>
  </div>
    
    
  </div>
  

</header>

<div class="cell">
<div class="sourceCode cell-code" id="cb1"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb1-1"><a href="#cb1-1" aria-hidden="true" tabindex="-1"></a><span class="do">##install.packages("datapasta")</span></span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<section id="is-pertussis-on-the-rise" class="level2">
<h2 class="anchored" data-anchor-id="is-pertussis-on-the-rise">Is Pertussis on the rise</h2>
<p>Scrape the CDC data on Pertussis cases per year in the US from their website here:</p>
<p>https://www.cdc.gov/pertussis/surv-reporting/cases-by-year.html</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb2"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb2-1"><a href="#cb2-1" aria-hidden="true" tabindex="-1"></a>cdc <span class="ot">&lt;-</span> <span class="fu">data.frame</span>(</span>
<span id="cb2-2"><a href="#cb2-2" aria-hidden="true" tabindex="-1"></a>                                 <span class="at">Year =</span> <span class="fu">c</span>(1922L,1923L,1924L,1925L,</span>
<span id="cb2-3"><a href="#cb2-3" aria-hidden="true" tabindex="-1"></a>                                          1926L,1927L,1928L,1929L,1930L,1931L,</span>
<span id="cb2-4"><a href="#cb2-4" aria-hidden="true" tabindex="-1"></a>                                          1932L,1933L,1934L,1935L,1936L,</span>
<span id="cb2-5"><a href="#cb2-5" aria-hidden="true" tabindex="-1"></a>                                          1937L,1938L,1939L,1940L,1941L,1942L,</span>
<span id="cb2-6"><a href="#cb2-6" aria-hidden="true" tabindex="-1"></a>                                          1943L,1944L,1945L,1946L,1947L,</span>
<span id="cb2-7"><a href="#cb2-7" aria-hidden="true" tabindex="-1"></a>                                          1948L,1949L,1950L,1951L,1952L,</span>
<span id="cb2-8"><a href="#cb2-8" aria-hidden="true" tabindex="-1"></a>                                          1953L,1954L,1955L,1956L,1957L,1958L,</span>
<span id="cb2-9"><a href="#cb2-9" aria-hidden="true" tabindex="-1"></a>                                          1959L,1960L,1961L,1962L,1963L,</span>
<span id="cb2-10"><a href="#cb2-10" aria-hidden="true" tabindex="-1"></a>                                          1964L,1965L,1966L,1967L,1968L,1969L,</span>
<span id="cb2-11"><a href="#cb2-11" aria-hidden="true" tabindex="-1"></a>                                          1970L,1971L,1972L,1973L,1974L,</span>
<span id="cb2-12"><a href="#cb2-12" aria-hidden="true" tabindex="-1"></a>                                          1975L,1976L,1977L,1978L,1979L,1980L,</span>
<span id="cb2-13"><a href="#cb2-13" aria-hidden="true" tabindex="-1"></a>                                          1981L,1982L,1983L,1984L,1985L,</span>
<span id="cb2-14"><a href="#cb2-14" aria-hidden="true" tabindex="-1"></a>                                          1986L,1987L,1988L,1989L,1990L,</span>
<span id="cb2-15"><a href="#cb2-15" aria-hidden="true" tabindex="-1"></a>                                          1991L,1992L,1993L,1994L,1995L,1996L,</span>
<span id="cb2-16"><a href="#cb2-16" aria-hidden="true" tabindex="-1"></a>                                          1997L,1998L,1999L,2000L,2001L,</span>
<span id="cb2-17"><a href="#cb2-17" aria-hidden="true" tabindex="-1"></a>                                          2002L,2003L,2004L,2005L,2006L,2007L,</span>
<span id="cb2-18"><a href="#cb2-18" aria-hidden="true" tabindex="-1"></a>                                          2008L,2009L,2010L,2011L,2012L,</span>
<span id="cb2-19"><a href="#cb2-19" aria-hidden="true" tabindex="-1"></a>                                          2013L,2014L,2015L,2016L,2017L,2018L,</span>
<span id="cb2-20"><a href="#cb2-20" aria-hidden="true" tabindex="-1"></a>                                          2019L),</span>
<span id="cb2-21"><a href="#cb2-21" aria-hidden="true" tabindex="-1"></a>         <span class="at">No..Reported.Pertussis.Cases =</span> <span class="fu">c</span>(<span class="dv">107473</span>,<span class="dv">164191</span>,<span class="dv">165418</span>,<span class="dv">152003</span>,</span>
<span id="cb2-22"><a href="#cb2-22" aria-hidden="true" tabindex="-1"></a>                                          <span class="dv">202210</span>,<span class="dv">181411</span>,<span class="dv">161799</span>,<span class="dv">197371</span>,</span>
<span id="cb2-23"><a href="#cb2-23" aria-hidden="true" tabindex="-1"></a>                                          <span class="dv">166914</span>,<span class="dv">172559</span>,<span class="dv">215343</span>,<span class="dv">179135</span>,<span class="dv">265269</span>,</span>
<span id="cb2-24"><a href="#cb2-24" aria-hidden="true" tabindex="-1"></a>                                          <span class="dv">180518</span>,<span class="dv">147237</span>,<span class="dv">214652</span>,<span class="dv">227319</span>,<span class="dv">103188</span>,</span>
<span id="cb2-25"><a href="#cb2-25" aria-hidden="true" tabindex="-1"></a>                                          <span class="dv">183866</span>,<span class="dv">222202</span>,<span class="dv">191383</span>,<span class="dv">191890</span>,<span class="dv">109873</span>,</span>
<span id="cb2-26"><a href="#cb2-26" aria-hidden="true" tabindex="-1"></a>                                          <span class="dv">133792</span>,<span class="dv">109860</span>,<span class="dv">156517</span>,<span class="dv">74715</span>,<span class="dv">69479</span>,</span>
<span id="cb2-27"><a href="#cb2-27" aria-hidden="true" tabindex="-1"></a>                                          <span class="dv">120718</span>,<span class="dv">68687</span>,<span class="dv">45030</span>,<span class="dv">37129</span>,<span class="dv">60886</span>,</span>
<span id="cb2-28"><a href="#cb2-28" aria-hidden="true" tabindex="-1"></a>                                          <span class="dv">62786</span>,<span class="dv">31732</span>,<span class="dv">28295</span>,<span class="dv">32148</span>,<span class="dv">40005</span>,</span>
<span id="cb2-29"><a href="#cb2-29" aria-hidden="true" tabindex="-1"></a>                                          <span class="dv">14809</span>,<span class="dv">11468</span>,<span class="dv">17749</span>,<span class="dv">17135</span>,<span class="dv">13005</span>,<span class="dv">6799</span>,</span>
<span id="cb2-30"><a href="#cb2-30" aria-hidden="true" tabindex="-1"></a>                                          <span class="dv">7717</span>,<span class="dv">9718</span>,<span class="dv">4810</span>,<span class="dv">3285</span>,<span class="dv">4249</span>,<span class="dv">3036</span>,</span>
<span id="cb2-31"><a href="#cb2-31" aria-hidden="true" tabindex="-1"></a>                                          <span class="dv">3287</span>,<span class="dv">1759</span>,<span class="dv">2402</span>,<span class="dv">1738</span>,<span class="dv">1010</span>,<span class="dv">2177</span>,<span class="dv">2063</span>,</span>
<span id="cb2-32"><a href="#cb2-32" aria-hidden="true" tabindex="-1"></a>                                          <span class="dv">1623</span>,<span class="dv">1730</span>,<span class="dv">1248</span>,<span class="dv">1895</span>,<span class="dv">2463</span>,<span class="dv">2276</span>,</span>
<span id="cb2-33"><a href="#cb2-33" aria-hidden="true" tabindex="-1"></a>                                          <span class="dv">3589</span>,<span class="dv">4195</span>,<span class="dv">2823</span>,<span class="dv">3450</span>,<span class="dv">4157</span>,<span class="dv">4570</span>,</span>
<span id="cb2-34"><a href="#cb2-34" aria-hidden="true" tabindex="-1"></a>                                          <span class="dv">2719</span>,<span class="dv">4083</span>,<span class="dv">6586</span>,<span class="dv">4617</span>,<span class="dv">5137</span>,<span class="dv">7796</span>,<span class="dv">6564</span>,</span>
<span id="cb2-35"><a href="#cb2-35" aria-hidden="true" tabindex="-1"></a>                                          <span class="dv">7405</span>,<span class="dv">7298</span>,<span class="dv">7867</span>,<span class="dv">7580</span>,<span class="dv">9771</span>,<span class="dv">11647</span>,</span>
<span id="cb2-36"><a href="#cb2-36" aria-hidden="true" tabindex="-1"></a>                                          <span class="dv">25827</span>,<span class="dv">25616</span>,<span class="dv">15632</span>,<span class="dv">10454</span>,<span class="dv">13278</span>,</span>
<span id="cb2-37"><a href="#cb2-37" aria-hidden="true" tabindex="-1"></a>                                          <span class="dv">16858</span>,<span class="dv">27550</span>,<span class="dv">18719</span>,<span class="dv">48277</span>,<span class="dv">28639</span>,<span class="dv">32971</span>,</span>
<span id="cb2-38"><a href="#cb2-38" aria-hidden="true" tabindex="-1"></a>                                          <span class="dv">20762</span>,<span class="dv">17972</span>,<span class="dv">18975</span>,<span class="dv">15609</span>,<span class="dv">18617</span>)</span>
<span id="cb2-39"><a href="#cb2-39" aria-hidden="true" tabindex="-1"></a>       )</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb3"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb3-1"><a href="#cb3-1" aria-hidden="true" tabindex="-1"></a><span class="fu">View</span>(cdc)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb4"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb4-1"><a href="#cb4-1" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(ggplot2)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<p>##Q1. With the help of the R “addin” package datapasta assign the CDC pertussis case number data to a data frame called cdc and use ggplot to make a plot of cases numbers over time.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb5"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb5-1"><a href="#cb5-1" aria-hidden="true" tabindex="-1"></a><span class="fu">ggplot</span>(cdc) <span class="sc">+</span></span>
<span id="cb5-2"><a href="#cb5-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">aes</span>(Year, No..Reported.Pertussis.Cases) <span class="sc">+</span></span>
<span id="cb5-3"><a href="#cb5-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_point</span>() <span class="sc">+</span></span>
<span id="cb5-4"><a href="#cb5-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_line</span>() <span class="sc">+</span></span>
<span id="cb5-5"><a href="#cb5-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">labs</span>(<span class="at">x=</span><span class="st">"year"</span>, <span class="at">y=</span><span class="st">"No.Reported.Pertussis.Cases"</span>, <span class="at">title=</span><span class="st">"Pertussis Cases by Year(1922-2019)"</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-19_files/figure-html/unnamed-chunk-5-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb6"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb6-1"><a href="#cb6-1" aria-hidden="true" tabindex="-1"></a>baseplot <span class="ot">&lt;-</span> <span class="fu">ggplot</span>(cdc) <span class="sc">+</span></span>
<span id="cb6-2"><a href="#cb6-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">aes</span>(Year, No..Reported.Pertussis.Cases) <span class="sc">+</span></span>
<span id="cb6-3"><a href="#cb6-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_point</span>() <span class="sc">+</span></span>
<span id="cb6-4"><a href="#cb6-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_line</span>() <span class="sc">+</span></span>
<span id="cb6-5"><a href="#cb6-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">labs</span>(<span class="at">x=</span><span class="st">"year"</span>, <span class="at">y=</span><span class="st">"No.Reported.Pertussis.Cases"</span>, <span class="at">title=</span><span class="st">"Pertussis Cases by Year(1922-2019)"</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<p>##Q2. Using the ggplot geom_vline() function add lines to your previous plot for the 1946 introduction of the wP vaccine and the 1996 switch to aP vaccine (see example in the hint below). What do you notice?</p>
<p>I noticed that there was a drastic decrease of number of reported Pertussis cases between 1946 and 1996. The number of reported Pertussis cases were very low by year ~1960 and stayed low until ~2002. After ~2002 there was a small increase of reported cases.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb7"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb7-1"><a href="#cb7-1" aria-hidden="true" tabindex="-1"></a><span class="fu">ggplot</span>(cdc) <span class="sc">+</span></span>
<span id="cb7-2"><a href="#cb7-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">aes</span>(Year, No..Reported.Pertussis.Cases) <span class="sc">+</span></span>
<span id="cb7-3"><a href="#cb7-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_point</span>() <span class="sc">+</span></span>
<span id="cb7-4"><a href="#cb7-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_line</span>() <span class="sc">+</span> <span class="fu">geom_vline</span>(<span class="at">xintercept=</span><span class="dv">1996</span>) <span class="sc">+</span> <span class="fu">geom_vline</span>(<span class="at">xintercept=</span><span class="dv">1946</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-19_files/figure-html/unnamed-chunk-7-1.png" class="img-fluid" width="672"></p>
</div>
<div class="sourceCode cell-code" id="cb8"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb8-1"><a href="#cb8-1" aria-hidden="true" tabindex="-1"></a>  <span class="fu">labs</span>(<span class="at">x=</span><span class="st">"year"</span>, <span class="at">y=</span><span class="st">"No.Reported.Pertussis.Cases"</span>, <span class="at">title=</span><span class="st">"Pertussis Cases by Year(1922-2019)"</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>$x
[1] "year"

$y
[1] "No.Reported.Pertussis.Cases"

$title
[1] "Pertussis Cases by Year(1922-2019)"

attr(,"class")
[1] "labels"</code></pre>
</div>
</div>
<p>There are two main Pertussis vaccine types, so-called whole-cell Pertusis (wP) and acellular Pertussis vaccines (aP). The older wP was introduced in 1946 and was highly effective. The switch to aP was in 1996.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb10"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb10-1"><a href="#cb10-1" aria-hidden="true" tabindex="-1"></a>baseplot <span class="sc">+</span> <span class="fu">geom_vline</span>(<span class="at">xintercept =</span> <span class="dv">1946</span>, <span class="at">color=</span><span class="st">"red"</span>, <span class="at">linetype=</span><span class="dv">2</span>) <span class="sc">+</span> <span class="fu">geom_vline</span>(<span class="at">xintercept =</span> <span class="dv">1996</span>, <span class="at">color=</span><span class="st">"blue"</span>, <span class="at">linetype=</span><span class="dv">2</span>) <span class="sc">+</span> <span class="fu">geom_text</span>(<span class="at">x=</span><span class="dv">1948</span>, <span class="at">y=</span><span class="dv">250000</span>, <span class="at">label=</span><span class="st">"wP"</span>, <span class="at">col=</span><span class="st">"red"</span>) <span class="sc">+</span> <span class="fu">geom_text</span>(<span class="at">x=</span><span class="dv">1998</span>, <span class="at">y=</span><span class="dv">250000</span>, <span class="at">label=</span><span class="st">"aP"</span>, <span class="at">col=</span><span class="st">"blue"</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-19_files/figure-html/unnamed-chunk-8-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<p>##Q3. Describe what happened after the introduction of the aP vaccine? Do you have a possible explanation for the observed trend?</p>
<p>After the introduction of aP vaccine the number of reported Pertussis cases began to slightly increase. I think introducing a new type of Pertussis vaccine created a fear towards the new type of vaccine causing the population to not get vaccinated anymore due to fear.</p>
</section>
<section id="the-cmi-pb-database" class="level1">
<h1>The CMI-PB database</h1>
<p>The CMI-RB project and associated database is making data on the immune response to Pertussis boost available to the scientific community.</p>
<p>We will see what type of data CMI-PB make available here in a moment.</p>
<p>First we need to be able to read data from CMI-PB. It, like many large advanced databases, returns JSON format.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb11"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb11-1"><a href="#cb11-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Allows us to read, write and process JSON data</span></span>
<span id="cb11-2"><a href="#cb11-2" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(jsonlite)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb12"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb12-1"><a href="#cb12-1" aria-hidden="true" tabindex="-1"></a>subject <span class="ot">&lt;-</span> <span class="fu">read_json</span>(<span class="st">"https://www.cmi-pb.org/api/subject"</span>, <span class="at">simplifyVector =</span> <span class="cn">TRUE</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb13"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb13-1"><a href="#cb13-1" aria-hidden="true" tabindex="-1"></a><span class="fu">head</span>(subject, <span class="dv">3</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>  subject_id infancy_vac biological_sex              ethnicity  race
1          1          wP         Female Not Hispanic or Latino White
2          2          wP         Female Not Hispanic or Latino White
3          3          wP         Female                Unknown White
  year_of_birth date_of_boost      dataset
1    1986-01-01    2016-09-12 2020_dataset
2    1968-01-01    2019-01-28 2020_dataset
3    1983-01-01    2016-10-10 2020_dataset</code></pre>
</div>
</div>
<p>##Q4. How many aP and wP infancy vaccinated subjects are in the dataset?</p>
<p>There are 47 aP infancy vaccinated subjects. There are 49 wP infancy vaccinated subjects.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb15"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb15-1"><a href="#cb15-1" aria-hidden="true" tabindex="-1"></a><span class="fu">table</span>(subject<span class="sc">$</span>infancy_vac)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>
aP wP 
47 49 </code></pre>
</div>
</div>
<p>##Q5. How many Male and Female subjects/patients are in the dataset?</p>
<p>There are 66 female subjects and 30 male subjects in the dataset.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb17"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb17-1"><a href="#cb17-1" aria-hidden="true" tabindex="-1"></a><span class="fu">table</span>(subject<span class="sc">$</span>biological_sex)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>
Female   Male 
    66     30 </code></pre>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb19"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb19-1"><a href="#cb19-1" aria-hidden="true" tabindex="-1"></a><span class="co">#View(subject)</span></span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<p>##Q6. What is the breakdown of race and biological sex (e.g.&nbsp;number of Asian females, White males etc…)?</p>
<p>American Indian/Alaska Native: 0 Females, 1 Male Asian: 18 Females, 9 Males Black or African American: 2 Females, 0 Male More Than One Race: 8 Females, 2 Males Native Hawaiian or Other Pacific Islander: 1 Female, 1 Male Unknown or Not Reported: 10 Females, 4 Males White: 27 Females, 13 Males</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb20"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb20-1"><a href="#cb20-1" aria-hidden="true" tabindex="-1"></a><span class="fu">table</span>(subject<span class="sc">$</span>race, subject<span class="sc">$</span>biological_sex)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>                                           
                                            Female Male
  American Indian/Alaska Native                  0    1
  Asian                                         18    9
  Black or African American                      2    0
  More Than One Race                             8    2
  Native Hawaiian or Other Pacific Islander      1    1
  Unknown or Not Reported                       10    4
  White                                         27   13</code></pre>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb22"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb22-1"><a href="#cb22-1" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(lubridate)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stderr">
<pre><code>Loading required package: timechange</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>
Attaching package: 'lubridate'</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>The following objects are masked from 'package:base':

    date, intersect, setdiff, union</code></pre>
</div>
</div>
<p>##What is today’s date?</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb26"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb26-1"><a href="#cb26-1" aria-hidden="true" tabindex="-1"></a><span class="fu">today</span>()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] "2022-12-02"</code></pre>
</div>
</div>
<p>##How many days have passed since new year 2000?</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb28"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb28-1"><a href="#cb28-1" aria-hidden="true" tabindex="-1"></a><span class="fu">today</span>() <span class="sc">-</span> <span class="fu">ymd</span>(<span class="st">"2000-01-01"</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>Time difference of 8371 days</code></pre>
</div>
</div>
<p>##What is this in years?</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb30"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb30-1"><a href="#cb30-1" aria-hidden="true" tabindex="-1"></a><span class="fu">time_length</span>( <span class="fu">today</span>() <span class="sc">-</span> <span class="fu">ymd</span>(<span class="st">"2000-01-01"</span>),  <span class="st">"years"</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 22.91855</code></pre>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb32"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb32-1"><a href="#cb32-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Use todays date to calculate age in days</span></span>
<span id="cb32-2"><a href="#cb32-2" aria-hidden="true" tabindex="-1"></a>subject<span class="sc">$</span>age <span class="ot">&lt;-</span> <span class="fu">time_length</span>( <span class="fu">today</span>() <span class="sc">-</span> <span class="fu">ymd</span>(subject<span class="sc">$</span>year_of_birth), <span class="st">"years"</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb33"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb33-1"><a href="#cb33-1" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(dplyr)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stderr">
<pre><code>
Attaching package: 'dplyr'</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>The following objects are masked from 'package:stats':

    filter, lag</code></pre>
</div>
<div class="cell-output cell-output-stderr">
<pre><code>The following objects are masked from 'package:base':

    intersect, setdiff, setequal, union</code></pre>
</div>
<div class="sourceCode cell-code" id="cb37"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb37-1"><a href="#cb37-1" aria-hidden="true" tabindex="-1"></a>ap <span class="ot">&lt;-</span> subject <span class="sc">%&gt;%</span> <span class="fu">filter</span>(infancy_vac <span class="sc">==</span> <span class="st">"aP"</span>)</span>
<span id="cb37-2"><a href="#cb37-2" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb37-3"><a href="#cb37-3" aria-hidden="true" tabindex="-1"></a><span class="fu">round</span>( <span class="fu">summary</span>(ap<span class="sc">$</span>age))</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
     23      25      26      25      26      27 </code></pre>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb39"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb39-1"><a href="#cb39-1" aria-hidden="true" tabindex="-1"></a>wp <span class="ot">&lt;-</span> subject <span class="sc">%&gt;%</span> <span class="fu">filter</span>(infancy_vac <span class="sc">==</span> <span class="st">"wP"</span>)</span>
<span id="cb39-2"><a href="#cb39-2" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb39-3"><a href="#cb39-3" aria-hidden="true" tabindex="-1"></a><span class="fu">round</span>( <span class="fu">summary</span>(wp<span class="sc">$</span>age))</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
     28      32      35      36      40      55 </code></pre>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb41"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb41-1"><a href="#cb41-1" aria-hidden="true" tabindex="-1"></a><span class="fu">t.test</span>(ap<span class="sc">$</span>age, wp<span class="sc">$</span>age)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>
    Welch Two Sample t-test

data:  ap$age and wp$age
t = -12.092, df = 51.082, p-value &lt; 2.2e-16
alternative hypothesis: true difference in means is not equal to 0
95 percent confidence interval:
 -12.644857  -9.044045
sample estimates:
mean of x mean of y 
 25.23634  36.08079 </code></pre>
</div>
</div>
<p>##Q7. Using this approach determine (i) the average age of wP individuals, (ii) the average age of aP individuals; and (iii) are they significantly different?</p>
<p>The average age of wP individuals is 36.</p>
<p>The average age of aP individuals is 25.</p>
<p>Based off the p-value (2.2e-16) obtained from a T-test, it demonstrates that they are are significantly different.</p>
<p>##Q8. Determine the age of all individuals at time of boost?</p>
<p>The ages of all individuals at time of boost are 30, 51, 33, 28, 25 and 28.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb43"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb43-1"><a href="#cb43-1" aria-hidden="true" tabindex="-1"></a>int <span class="ot">&lt;-</span> <span class="fu">ymd</span>(subject<span class="sc">$</span>date_of_boost) <span class="sc">-</span> <span class="fu">ymd</span>(subject<span class="sc">$</span>year_of_birth)</span>
<span id="cb43-2"><a href="#cb43-2" aria-hidden="true" tabindex="-1"></a>age_at_boost <span class="ot">&lt;-</span> <span class="fu">time_length</span>(int, <span class="st">"year"</span>)</span>
<span id="cb43-3"><a href="#cb43-3" aria-hidden="true" tabindex="-1"></a><span class="fu">head</span>(age_at_boost)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 30.69678 51.07461 33.77413 28.65982 25.65914 28.77481</code></pre>
</div>
</div>
<p>What is the average age across all subjects?</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb45"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb45-1"><a href="#cb45-1" aria-hidden="true" tabindex="-1"></a><span class="fu">summary</span>(subject<span class="sc">$</span>age)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
  22.92   25.92   27.92   30.77   34.92   54.92 </code></pre>
</div>
</div>
<p>Histogram</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb47"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb47-1"><a href="#cb47-1" aria-hidden="true" tabindex="-1"></a><span class="fu">ggplot</span>(subject) <span class="sc">+</span> <span class="fu">aes</span>(age)<span class="sc">+</span> <span class="fu">geom_histogram</span>()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stderr">
<pre><code>`stat_bin()` using `bins = 30`. Pick better value with `binwidth`.</code></pre>
</div>
<div class="cell-output-display">
<p><img src="Lab-19_files/figure-html/unnamed-chunk-26-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<p>And faceted by wP and aP</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb49"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb49-1"><a href="#cb49-1" aria-hidden="true" tabindex="-1"></a><span class="fu">ggplot</span>(subject) <span class="sc">+</span></span>
<span id="cb49-2"><a href="#cb49-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">aes</span>(<span class="fu">time_length</span>(age, <span class="st">"year"</span>),</span>
<span id="cb49-3"><a href="#cb49-3" aria-hidden="true" tabindex="-1"></a>      <span class="at">fill=</span><span class="fu">as.factor</span>(infancy_vac)) <span class="sc">+</span></span>
<span id="cb49-4"><a href="#cb49-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_histogram</span>(<span class="at">show.legend=</span><span class="cn">FALSE</span>) <span class="sc">+</span></span>
<span id="cb49-5"><a href="#cb49-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">facet_wrap</span>(<span class="fu">vars</span>(infancy_vac), <span class="at">nrow=</span><span class="dv">2</span>) </span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stderr">
<pre><code>`stat_bin()` using `bins = 30`. Pick better value with `binwidth`.</code></pre>
</div>
<div class="cell-output-display">
<p><img src="Lab-19_files/figure-html/unnamed-chunk-27-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb51"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb51-1"><a href="#cb51-1" aria-hidden="true" tabindex="-1"></a>x <span class="ot">&lt;-</span> <span class="fu">t.test</span>(<span class="fu">time_length</span>( wp<span class="sc">$</span>age, <span class="st">"years"</span> ),</span>
<span id="cb51-2"><a href="#cb51-2" aria-hidden="true" tabindex="-1"></a>       <span class="fu">time_length</span>( ap<span class="sc">$</span>age, <span class="st">"years"</span> ))</span>
<span id="cb51-3"><a href="#cb51-3" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb51-4"><a href="#cb51-4" aria-hidden="true" tabindex="-1"></a>x<span class="sc">$</span>p.value</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 1.316045e-16</code></pre>
</div>
</div>
<p>##Q9. With the help of a faceted boxplot or histogram, do you think these two groups are significantly different?</p>
<p>Yes, based off the p-value (1.316045e-16) both groups are significantly different.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb53"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb53-1"><a href="#cb53-1" aria-hidden="true" tabindex="-1"></a>specimen <span class="ot">&lt;-</span> <span class="fu">read_json</span>(<span class="st">"https://www.cmi-pb.org/api/specimen"</span>, <span class="at">simplifyVector =</span> <span class="cn">TRUE</span>) </span>
<span id="cb53-2"><a href="#cb53-2" aria-hidden="true" tabindex="-1"></a>titer <span class="ot">&lt;-</span> <span class="fu">read_json</span>(<span class="st">"https://www.cmi-pb.org/api/ab_titer"</span>, <span class="at">simplifyVector =</span> <span class="cn">TRUE</span>) </span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb54"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb54-1"><a href="#cb54-1" aria-hidden="true" tabindex="-1"></a><span class="fu">head</span>(specimen)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>  specimen_id subject_id actual_day_relative_to_boost
1           1          1                           -3
2           2          1                          736
3           3          1                            1
4           4          1                            3
5           5          1                            7
6           6          1                           11
  planned_day_relative_to_boost specimen_type visit
1                             0         Blood     1
2                           736         Blood    10
3                             1         Blood     2
4                             3         Blood     3
5                             7         Blood     4
6                            14         Blood     5</code></pre>
</div>
</div>
<p>We want to “join” the ‘subject’ and ‘specimen’ tables to have all the metadata we need for later analysis. We can use the dplyr ’*_join()’ functions for this task.</p>
<p>##Q9. Complete the code to join specimen and subject tables to make a new merged data frame containing all specimen records along with their associated subject details:</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb56"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb56-1"><a href="#cb56-1" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(dplyr)</span>
<span id="cb56-2"><a href="#cb56-2" aria-hidden="true" tabindex="-1"></a>meta <span class="ot">&lt;-</span> <span class="fu">inner_join</span>(specimen, subject)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stderr">
<pre><code>Joining, by = "subject_id"</code></pre>
</div>
<div class="sourceCode cell-code" id="cb58"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb58-1"><a href="#cb58-1" aria-hidden="true" tabindex="-1"></a><span class="fu">dim</span>(meta)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 729  14</code></pre>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb60"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb60-1"><a href="#cb60-1" aria-hidden="true" tabindex="-1"></a>titer <span class="ot">&lt;-</span> <span class="fu">read_json</span>(<span class="st">"http://cmi-pb.org/api/ab_titer"</span>, <span class="at">simplifyVector =</span> <span class="cn">TRUE</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb61"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb61-1"><a href="#cb61-1" aria-hidden="true" tabindex="-1"></a><span class="fu">head</span>(titer)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>  specimen_id isotype is_antigen_specific antigen        MFI MFI_normalised
1           1     IgE               FALSE   Total 1110.21154       2.493425
2           1     IgE               FALSE   Total 2708.91616       2.493425
3           1     IgG                TRUE      PT   68.56614       3.736992
4           1     IgG                TRUE     PRN  332.12718       2.602350
5           1     IgG                TRUE     FHA 1887.12263      34.050956
6           1     IgE                TRUE     ACT    0.10000       1.000000
   unit lower_limit_of_detection
1 UG/ML                 2.096133
2 IU/ML                29.170000
3 IU/ML                 0.530000
4 IU/ML                 6.205949
5 IU/ML                 4.679535
6 IU/ML                 2.816431</code></pre>
</div>
</div>
<p>I need to link a.k.a join this ab titer data with our meta data to have all the information we need to do some actual analysis like comparing Ab levels at different times after boost, comparing ap vs wP responses over time etc.</p>
<p>##Q10. Now using the same procedure join meta with titer data so we can further analyze this data in terms of time of visit aP/wP, male/female etc.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb63"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb63-1"><a href="#cb63-1" aria-hidden="true" tabindex="-1"></a>abdata <span class="ot">&lt;-</span> <span class="fu">inner_join</span>(titer, meta)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stderr">
<pre><code>Joining, by = "specimen_id"</code></pre>
</div>
<div class="sourceCode cell-code" id="cb65"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb65-1"><a href="#cb65-1" aria-hidden="true" tabindex="-1"></a><span class="fu">dim</span>(abdata)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>[1] 32675    21</code></pre>
</div>
</div>
<p>##Q11. How many specimens (i.e.&nbsp;entries in abdata) do we have for each isotype?</p>
<p>IgE: 6698 IgG: 1413 IgG1: 6141 IgG2: 6141 IgG3: 6141 IgG4: 6141</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb67"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb67-1"><a href="#cb67-1" aria-hidden="true" tabindex="-1"></a><span class="fu">table</span>(abdata<span class="sc">$</span>isotype)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>
 IgE  IgG IgG1 IgG2 IgG3 IgG4 
6698 1413 6141 6141 6141 6141 </code></pre>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb69"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb69-1"><a href="#cb69-1" aria-hidden="true" tabindex="-1"></a><span class="fu">ggplot</span>(abdata) <span class="sc">+</span> <span class="fu">aes</span>(MFI, antigen) <span class="sc">+</span> <span class="fu">geom_boxplot</span>()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stderr">
<pre><code>Warning: Removed 1 rows containing non-finite values (`stat_boxplot()`).</code></pre>
</div>
<div class="cell-output-display">
<p><img src="Lab-19_files/figure-html/unnamed-chunk-36-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb71"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb71-1"><a href="#cb71-1" aria-hidden="true" tabindex="-1"></a><span class="fu">ggplot</span>(abdata) <span class="sc">+</span> <span class="fu">aes</span>(MFI_normalised, antigen) <span class="sc">+</span> <span class="fu">geom_boxplot</span>()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-19_files/figure-html/unnamed-chunk-37-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<p>##Q12. What do you notice about the number of visit 8 specimens compared to other visits?</p>
<p>I notice that the number of visit 8 specimens is much lower compared to the other visits.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb72"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb72-1"><a href="#cb72-1" aria-hidden="true" tabindex="-1"></a><span class="fu">table</span>(abdata<span class="sc">$</span>visit)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>
   1    2    3    4    5    6    7    8 
5795 4640 4640 4640 4640 4320 3920   80 </code></pre>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb74"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb74-1"><a href="#cb74-1" aria-hidden="true" tabindex="-1"></a>ig1 <span class="ot">&lt;-</span> abdata <span class="sc">%&gt;%</span> <span class="fu">filter</span>(isotype <span class="sc">==</span> <span class="st">"IgG1"</span>, visit<span class="sc">!=</span><span class="dv">8</span>)</span>
<span id="cb74-2"><a href="#cb74-2" aria-hidden="true" tabindex="-1"></a><span class="fu">head</span>(ig1)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stdout">
<pre><code>  specimen_id isotype is_antigen_specific antigen        MFI MFI_normalised
1           1    IgG1                TRUE     ACT 274.355068      0.6928058
2           1    IgG1                TRUE     LOS  10.974026      2.1645083
3           1    IgG1                TRUE   FELD1   1.448796      0.8080941
4           1    IgG1                TRUE   BETV1   0.100000      1.0000000
5           1    IgG1                TRUE   LOLP1   0.100000      1.0000000
6           1    IgG1                TRUE Measles  36.277417      1.6638332
   unit lower_limit_of_detection subject_id actual_day_relative_to_boost
1 IU/ML                 3.848750          1                           -3
2 IU/ML                 4.357917          1                           -3
3 IU/ML                 2.699944          1                           -3
4 IU/ML                 1.734784          1                           -3
5 IU/ML                 2.550606          1                           -3
6 IU/ML                 4.438966          1                           -3
  planned_day_relative_to_boost specimen_type visit infancy_vac biological_sex
1                             0         Blood     1          wP         Female
2                             0         Blood     1          wP         Female
3                             0         Blood     1          wP         Female
4                             0         Blood     1          wP         Female
5                             0         Blood     1          wP         Female
6                             0         Blood     1          wP         Female
               ethnicity  race year_of_birth date_of_boost      dataset
1 Not Hispanic or Latino White    1986-01-01    2016-09-12 2020_dataset
2 Not Hispanic or Latino White    1986-01-01    2016-09-12 2020_dataset
3 Not Hispanic or Latino White    1986-01-01    2016-09-12 2020_dataset
4 Not Hispanic or Latino White    1986-01-01    2016-09-12 2020_dataset
5 Not Hispanic or Latino White    1986-01-01    2016-09-12 2020_dataset
6 Not Hispanic or Latino White    1986-01-01    2016-09-12 2020_dataset
       age
1 36.91718
2 36.91718
3 36.91718
4 36.91718
5 36.91718
6 36.91718</code></pre>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb76"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb76-1"><a href="#cb76-1" aria-hidden="true" tabindex="-1"></a><span class="fu">ggplot</span>(ig1) <span class="sc">+</span></span>
<span id="cb76-2"><a href="#cb76-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">aes</span>(MFI, antigen) <span class="sc">+</span></span>
<span id="cb76-3"><a href="#cb76-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_boxplot</span>()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-19_files/figure-html/unnamed-chunk-40-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<p>We can break this up by visit (a quick proxy for time since boost).</p>
<p>##Q13. Complete the following code to make a summary boxplot of Ab titer levels for all antigens:</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb77"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb77-1"><a href="#cb77-1" aria-hidden="true" tabindex="-1"></a><span class="fu">ggplot</span>(ig1) <span class="sc">+</span></span>
<span id="cb77-2"><a href="#cb77-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">aes</span>(MFI, antigen) <span class="sc">+</span></span>
<span id="cb77-3"><a href="#cb77-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_boxplot</span>() <span class="sc">+</span> </span>
<span id="cb77-4"><a href="#cb77-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">facet_wrap</span>(<span class="fu">vars</span>(visit), <span class="at">nrow=</span><span class="dv">2</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-19_files/figure-html/unnamed-chunk-41-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<p>##Q14. What antigens show differences in the level of IgG1 antibody titers recognizing them over time? Why these and not others? Antigen FIM2/3 shows the greatest difference in the level of IgG1 antibody titers recognizing them over time. Antigen FIM2/3 has the greatest difference over time because it might have been used for the development of the vaccine, which would affect the level of IgG1 antibody titers recognizing them over time.</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb78"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb78-1"><a href="#cb78-1" aria-hidden="true" tabindex="-1"></a><span class="fu">ggplot</span>(ig1) <span class="sc">+</span></span>
<span id="cb78-2"><a href="#cb78-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">aes</span>(MFI, antigen, <span class="at">col=</span>infancy_vac ) <span class="sc">+</span></span>
<span id="cb78-3"><a href="#cb78-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_boxplot</span>(<span class="at">show.legend =</span> <span class="cn">FALSE</span>) <span class="sc">+</span> </span>
<span id="cb78-4"><a href="#cb78-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">facet_wrap</span>(<span class="fu">vars</span>(visit), <span class="at">nrow=</span><span class="dv">2</span>) <span class="sc">+</span></span>
<span id="cb78-5"><a href="#cb78-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">theme_bw</span>()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-19_files/figure-html/unnamed-chunk-42-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<div class="cell">
<div class="sourceCode cell-code" id="cb79"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb79-1"><a href="#cb79-1" aria-hidden="true" tabindex="-1"></a><span class="fu">ggplot</span>(ig1) <span class="sc">+</span></span>
<span id="cb79-2"><a href="#cb79-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">aes</span>(MFI, antigen, <span class="at">col=</span>infancy_vac ) <span class="sc">+</span></span>
<span id="cb79-3"><a href="#cb79-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_boxplot</span>(<span class="at">show.legend =</span> <span class="cn">FALSE</span>) <span class="sc">+</span> </span>
<span id="cb79-4"><a href="#cb79-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">facet_wrap</span>(<span class="fu">vars</span>(infancy_vac, visit), <span class="at">nrow=</span><span class="dv">2</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-19_files/figure-html/unnamed-chunk-43-1.png" class="img-fluid" width="672"></p>
</div>
</div>
<p>##Q15. Filter to pull out only two specific antigens for analysis and create a boxplot for each. You can chose any you like. Below I picked a “control” antigen (“Measles”, that is not in our vaccines) and a clear antigen of interest (“FIM2/3”, extra-cellular fimbriae proteins from B. pertussis that participate in substrate attachment).</p>
<div class="cell">
<div class="sourceCode cell-code" id="cb80"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb80-1"><a href="#cb80-1" aria-hidden="true" tabindex="-1"></a><span class="fu">filter</span>(ig1, antigen<span class="sc">==</span><span class="st">"Measles"</span>) <span class="sc">%&gt;%</span></span>
<span id="cb80-2"><a href="#cb80-2" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ggplot</span>() <span class="sc">+</span></span>
<span id="cb80-3"><a href="#cb80-3" aria-hidden="true" tabindex="-1"></a>  <span class="fu">aes</span>(MFI, <span class="at">col=</span>infancy_vac) <span class="sc">+</span></span>
<span id="cb80-4"><a href="#cb80-4" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_boxplot</span>(<span class="at">show.legend =</span> <span class="cn">TRUE</span>) <span class="sc">+</span></span>
<span id="cb80-5"><a href="#cb80-5" aria-hidden="true" tabindex="-1"></a>  <span class="fu">facet_wrap</span>(<span class="fu">vars</span>(visit)) <span class="sc">+</span></span>
<span id="cb80-6"><a href="#cb80-6" aria-hidden="true" tabindex="-1"></a>  <span class="fu">theme_bw</span>()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output-display">
<p><img src="Lab-19_files/figure-html/unnamed-chunk-44-1.png" class="img-fluid" width="672"></p>
</div>
</div>
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