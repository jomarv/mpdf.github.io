---
layout: page
title: pagenumPrefix
parent_title: mPDF Variables
permalink: /reference/mpdf-variables/pagenumprefix.html
---

<div id="bpmbook" class="bpmbook" style="direction:ltr;">
<div class="topic_user_field">
<div id="U0">
<p>(mPDF &gt;= 3.0)</p>
<h2>Description</h2>

<div class="alert alert-info" role="alert">string <b>pagenumPrefix</b></div>
<p>Specify text to precede the page number when using {PAGENO} to insert page numbers in headers or footers.</p>

<div class="alert alert-info" role="alert"><b>Note:</b> This is only recommended in non-HTML headers and footers. Although the text is added correctly in HTML headers &amp; footers, the text alignment is not readjusted after substitution e.g. if it used in the right margin.</div>
<h2>Examples</h2>

{% highlight php %}
Example #1
{% endhighlight %}

{% highlight php %}
<?php

<?php

$mpdf=new mPDF();

$mpdf->pagenumPrefix = 'Page number ';

$mpdf->pagenumSuffix = ' - ';

$mpdf->nbpgPrefix = ' out of ';

$mpdf->nbpgSuffix = ' pages';

$mpdf->SetHeader('{PAGENO}{nbpg}');

$mpdf->WriteHTML("Hallo World");

$mpdf->Output();

?>
{% endhighlight %}

{% highlight php %}
Will output a header:

"Page number 1 - out of 1 pages"
{% endhighlight %}

<h2>See Also</h2>
<ul>
<li class="manual_boxlist"><a href="/reference/mpdf-variables/pagenumsuffix.html">pagenumSuffix</a> - Specify text to follow page numbers generated by {PAGENO}</li>
<li class="manual_boxlist"><a href="/reference/mpdf-variables/nbpgprefix.html">nbpgPrefix</a> - Specify text to precede page total generated by {nbpg}

</li>
<li class="manual_boxlist"><a href="/reference/mpdf-variables/nbpgsuffix.html">nbpgSuffix</a> - Specify text to follow page numbers generated by {nbpg}</li>
<li class="manual_boxlist"><a href="/paging/page-numbering.html">Page numbering</a> - 

</li>
<li class="manual_boxlist"><a href="/what-else-can-i-do/replaceable-aliases.html">Replaceable aliases</a> -&nbsp;</li>
<li class="manual_boxlist"><a href="/reference/mpdf-variables/aliasnbpg.html">aliasNbPg</a> - Specify the text to be replaced by the document page total</li>
<li class="manual_boxlist"><a href="/reference/mpdf-variables/aliasnbpggp.html">aliasNbPgGp</a> - Specify the text to be replaced by the group page total</li>
</ul>
<p>&nbsp;</p>
</div>
</div>
