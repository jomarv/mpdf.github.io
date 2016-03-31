---
layout: page
title: AliasNbPages()
parent_title: mPDF functions
permalink: /reference/mpdf-functions/aliasnbpages.html
---

<div id="bpmbook" class="bpmbook" style="direction:ltr;">
<div class="topic_user_field">
<div id="U0">
<p>(mPDF &gt;= 1.0)</p>
<p>AliasNbPages – Defines the placeholder used to insert total number of pages into the document</p>
<h2>Description</h2>

<div class="alert alert-info" role="alert">void <b>AliasNbPages</b> ( string <span class="parameter">$text</span> )</div>
<p>Set the value for the variable string <a href="/reference/mpdf-variables/aliasnbpg.html">aliasNbPg</a> which is used as a placeholder used to insert total number of pages into the document.</p>
<h2>Parameters</h2>
<p class="manual_param_dt"><span class="parameter">text</span></p>
<p class="manual_param_dd">Defines the text for the vaiable <span class="parameter">aliasNbPg</span>. 

<span class="smallblock">DEFAULT</span>: {nb}</p>
<h2>Examples</h2>

{% highlight php %}
Example #1
{% endhighlight %}

{% highlight php %}
<?php

<?php

$mpdf=new mPDF();

$mpdf->AliasNbPages('[pagetotal]');

$mpdf->WriteHTML('<p>There are [pagetotal] pages in this document</p>');

$mpdf->Output();

?>
{% endhighlight %}

{% highlight php %}
Example #2
{% endhighlight %}

{% highlight php %}
<?php

$mpdf->AliasNbPages('[pagetotal]');

is the exact equivalent of:

$mpdf->aliasNbPg = '[pagetotal]';
{% endhighlight %}

<h2>See Also</h2>
<ul>
<li class="manual_boxlist"><a href="/what-else-can-i-do/replaceable-aliases.html">Replaceable Aliases</a> 

</li>
<li class="manual_boxlist"><a href="/reference/mpdf-functions/aliasnbpagegroups.html">AliasNbPageGroups()</a> - Sets the placeholder alias for the total number of pages in a document or page group</li>
</ul>
</div>
</div>
