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

<p>Javascript runs on primarily on web browsers. It is also used in NodeJS which can be installed directly on to a OS utilizing chrome's v8 engine , javascript engines can be implemented on many devices and environments</p>


<p>Both these languages are afforded cross-platform ubiquity, appearing on multiple operating systems. 
However, neither language can be run on the other's runtime. C# will not run on the browser and Javascript is not compiled with .NET
  (Jscript notwithstanding) both languages are also evolving entities and it would serve us well to pick versions of them that we would like to compare.</p>

<p> While C# follows a standard, and is maintained by Microsoft, Javascript proves to be a little more complicated. </p>
<p>There are almost as many flavours of Javascript as there are JS engines. And this led to wildly differing implementations in its early years. Some semblance of uniformity was established when various interested parties decided to get the language standardized through the standards body 'ECMA' and now it has a official specification otherwise known as ECMAscript</p>

<p>For pratical reasons we shall limit ourselves to comparing C# latest version, 8 -  with ECMAscript 2015, otherwise known as 'ES 6', probably the most widely implemented specification </p>
<P>I hope to include relevant information about later versions of the ECMAscript standard when deemed appropiate</p>


## TYPES

 C# is a statically typed language and dependent on .NET CLR (Common Language Runtime ) 
 Types can be defined as different data-structures: classes; structs; enums; delegates; interfaces.
 Its primitive types, passed by value are: **int, object, short, char, float, double, char and bool**
 All types are in fact basically _object_ data structures and the primitive types are implemented as _structs_ 
 
 Javascript is dynamically typed: its types are established at runtime, although this gives less protection when authoring your code it does allow
 dynamic addition and deletion of object properties. It has 6 primitive types: **string, number, bigint, boolean, undefined, and symbol.**
 These primitive types are passed by value but are converted to equivalent objects when running methods on them.
 eg.
  **let x = 1234 ; x.toString()**  // "1234"   _x is read as a Number object and its 'toString' method is called to return "1234"_
 
<br/>
 
 ## COMPILATION
 
 ### C#
 <p>C# uses the Roselyn Compiler which is provided as part of the .NET Core SDK, and Visual Studio 2015 which means if you have .NET Core installed on your machine it will 
 include the Roselyn Compiler. Bear in mind that it is not included with .NET framework which uses an older compiler.</p>
 <p> Roselyn, unlike the older c# compiler , is open-source and extendable</p>
 
 Roselyn will take the source code and compile it down to a CIL (Common Intermeidate Language), otherwise known as an 'assembly'. The assembly will have an extension of *.dll*
 or _.exe_ . The CLR (Commonn Language Runtime) further uses a technique of _Just-In-Time_(JIT) compilation at runtime to convert the CIL into machine code. The JIT compiler may perform optimizations of the code as well as only compiling the code when needed.
 
 
 ### Javascript
 
 Javascript is known as an _interpreted_ language rather than a compiled language. The transformation of the source code happens at runtime.
 <p>As we mentioned, there are a multitude of Javascript runtimes, that are otherwise be known as Javscript Engines.</p>
<p>Most of the popular browsers implement their own javascript engine</p>
 <p>These days most engines work along similar lines that they use a combination of an interpretor and an compiler</p>
 
 
 
 ## CLASSES
 
  While both languages follow the object oriented paradigm they implement them in different ways.
  Javascript has prototypal inheritance whereas C# uses a more traditional 'classical'(class based) model.
   
   
   ### Javascript
   
   Pre ES2015 in order to create an object of a particular type one would use a constructor function - or simply 'constructor'.
   ```function Person(age, firstname, surname) {   // can pass in initial parameters for instant
        this.age = age ;             // an object called 'this' is implicitly created and we can assign properties to it
        this.firstName = firstname ; 
        this.surName = surname;
        this.getFullname = function() {              
            return this.firstName + " " + this.surname;   
