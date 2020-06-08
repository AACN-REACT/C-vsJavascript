# C# vs Javascript
Some notes on the differences between two languages


## Preface

<p>This is primarliy written for my own benefit, to help organise my learning of C# and .NET. </p>

<p>I hope that my learning of C# is aided by comparing it to something I am already familiar with, ie. javascript.</p>
<p>It may well be that those looking to go the other way may find some value in these notes.</p>
It is not meant as an authoritive reference on the subject and should not be treated as such.
On the contrary: this will be full of mistak.es and inaccuracies.
I shall try as much as possible to keep the style light, jargon-free and informative.
The orgainsition and ordering of these notes may appear haphazard.
<p>Nothwithstanding, I hope any one else who has stumbled upon this work manages to glean some insight or knowledge from it.</p>


## Runtimes and Versions

<p>Of course we wouldnt be able to compare the languages without also taking into account the systems that run them.
By that I mean their respective runtimes, the platforms which execute the code. This brings us to the first major difference between the two.</p>

<p>C# runs on .NET Standard compliant frameworks, this includes: </p>
<ul>
<li> .NET framework </li>
<li> .NET core </li>
<li> Xamarin</li>
<li> Mono</li>    
</ul>

<p>Javascript runs on primarily on web browsers, and NodeJS can be installed directly on to a OS while running on chrome's v8 engine , javascript engines can be implemented on many devices and environments</p>


<p>Both these languages are afforded cross-platform ubiquity, appearing on multiple operating systems. 
However, neither language can be run on the other's runtime. C# will not run on the browser and Javascript is not compiled with .NET
  (Jscript notwithstanding) both languages are also evolving entities and it would serve us well to pick versions of them that we would like to compare.</p>

<p> While C# follows a standard, and is maintained by Microsoft, Javascript proves to be a little more complicated. </p>
<p>There are almost as many flavours of Javascript as there are JS engines. And this led to wildly differing implementations in its early years. Some semblance of uniformity was established when various interested parties decided to get the language standardized through the standards body 'ECMA' and now it has a official specification otherwise known as ECMAscript</p>

<p>For pratical reasons we shall limit ourselves to comparing C# latest version, 8 -  with ECMAscript 2015, otherwise known as 'ECMAscript 6', probably the most widely implemented specification </p>
<P>I hope to include relevant information about later versions of the ECMAscript standard when deemed appropiate</p>
