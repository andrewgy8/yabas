---
layout:     post
title:      "Pgloader on Mac"
subtitle:   "Super simple migration tool"
date:       2017-05-30 4:00:00
author:     "Andrew Graham-Yooll"

---

<h2 class="section-heading">Getting Started</h2>
<p>The other day, we at Solaris Offgrid needed to port our database over to PostgreSQL.  It was time.</p>
<p>For that task we used the handy tool that <a href="http://pgloader.io/index.html">Dimitri Fontaine built.</a></p>

<p>I thought the instructions on installing the tool on a Mac could have been a bit clearer.  So I wrote it up.</p>


<ol>
	<li>In your terminal, clone the project onto your machine {% highlight bash %}git clone https://github.com/dimitri/pgloader.git{% endhighlight %}</li>
	<li>{% highlight bash %}brew install sbcl
brew install clozure-cl
brew install freetds --universal --build-from-source{% endhighlight %}
	</li>
	<li>{% highlight bash %}cd pgloader{% endhighlight %}</li>
	<li>You probably wont have to run {% highlight bash %}make{% endhighlight %} as the last command should have run that for you. That did it for me!</li>
	<li>{% highlight bash %}./build/bin/pgloader --version{% endhighlight %} Now it is installed.</li>
	<li>Create an alias for pgloader {% highlight bash %}nano ~/.bash-profile 
alias pgloader="copied path_to_here/build/bin/pgloader"{% endhighlight %}. Then cntrl + o, enter, cntrl + x</li>
	<li>Test again:{% highlight bash %}pgloader --version
pgloader --help{% endhighlight %}</li>
</ol>

<p>Voila!</p>

<p>Hope it helps! If it doesn't work, let me know and Ill help out as much as possible.</p>
