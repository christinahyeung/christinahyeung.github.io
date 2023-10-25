---
permalink: /testing/
title: "This page is for testing"
---

<h1>Testing what is seen as the computed property name<h1>

<p>Test 1: The most straightforward: text in element is the same as computed property name</p>
<a href="foo.html">Test 1: This is the accessible text</a>


<p>Test 2: Adding a title</p>
<a href="foo.html" title="This is a title">Test 2: This is body text</a>

<p>Test 3: There is title text and alt text on the image: screen reader should read both?</p>
<a href="foo.html" title ="This is test 3 title text"><img src="{{site.baseurl | prepend: site.url}}/assets/img/flower.png" alt="Pink flower" title='image title text'></a>


<p>Test 4: This is testing only alt text on the image: should be seen as both alt text, and computed name (pink flower)</p>
<a href="foo.html" test><img src="{{site.baseurl | prepend: site.url}}/assets/img/flower.png" alt="Pink flower"></a>

<p>Test 5: This is testing how ARIA labels override alt text: computed name should match ARIA label (acutal overriding text), and combine it with title text. Alt text should not be read</p>
<a href="foo.html"><img src="{{site.baseurl | prepend: site.url}}/assets/img/flower.png" alt="Pink flower" title = 'title 5 text' aria-label="Aria label text"></a>

<p>Test 6: This is showing how the div contents inside an a href can be reflected (and  repeated)</p>
<a href="foo.html">
        <img src="{{site.baseurl | prepend: site.url}}/assets/img/flower.png">
        <div class="bt-wrapper">
            <div class="bt-wrapper-inner">
                <div class="bt-sponsored">Line 1</div>
                <div class="bt-short-text">Line2</div>
                <div class="bt-long-text">Line3</div>
            </div>
        </div>
    </a>

<p>Test 7: Should combine alt text with div contents</p>
<a href="foo.html">
        <img src="{{site.baseurl | prepend: site.url}}/assets/img/flower.png" alt='this is a pink flower'>
        <div class="bt-wrapper">
            <div class="bt-wrapper-inner">
                <div class="bt-sponsored">Line 1</div>
                <div class="bt-short-text">Line2</div>
                <div class="bt-long-text">Line3</div>
            </div>
        </div>
    </a>

<p>Test 8: Back to overriding with ARIA-labels in the a tag</p>
<a href="foo.html" aria-label = 'arialabeltext'>
        <img src="{{site.baseurl | prepend: site.url}}/assets/img/flower.png" alt='this is a pink flower'>
        <div class="bt-wrapper">
            <div class="bt-wrapper-inner">
                <div class="bt-sponsored">Line 1</div>
                <div class="bt-short-text">Line2</div>
                <div class="bt-long-text">Line3</div>
            </div>
        </div>
    </a>

<p>Test 9: tabbable div with aria-role</p>
<div role="img" alt="heart" tabindex="0">
 ♥︎
 </div>
