---
permalink: /testing/
title: "This page is for testing"
---

<h1>Testing what is seen as the computed property name<h1>

<p>Test 1: The most straightforward: text in element is the same as computed property name</p>
<a href="foo.html">Test 1: This is the accessible text</a>


<p>Test 2: Adding a title</p>
<a href="foo.html" title='Test 2 this is the accessible text'></a>

<p>Test 3: Overriding a title</p>
<a href="foo.html" title='Test 3 not seen'>This is the property name</a>

<p>Test 4: This is testing alt text: should be seen as both alt text, and computed name (pink flower)</p>
<a href="foo.html"><img src="flower.png" alt="Pink flower"></a>

<p>Test 5: This is testing how ARIA labels override alt text: computed name should match ARIA label (acutal overriding text), and alt-text should appear crossed out</p>
<a href="foo.html"><img src="flower.png" alt="Pink flower" aria-label="Actual overriding text"></a>

<p>Test 6: This is showing how the div contents inside an a href can be reflected (and  repeated)</p>
<a href="foo.html">
        <img src="flower.png">
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
        <img src="flower.png" alt='this should be hidden'>
        <div class="bt-wrapper">
            <div class="bt-wrapper-inner">
                <div class="bt-sponsored">Line 1</div>
                <div class="bt-short-text">Line2</div>
                <div class="bt-long-text">Line3</div>
            </div>
        </div>
    </a>

<p>Test 8: Back to overriding with ARIA-labels</p>
<a href="foo.html" aria-label='test'>
        <img src="flower.png" alt='this should be hidden'>
        <div class="bt-wrapper">
            <div class="bt-wrapper-inner">
                <div class="bt-sponsored">Line 1</div>
                <div class="bt-short-text">Line2</div>
                <div class="bt-long-text">Line3</div>
            </div>
        </div>
    </a>