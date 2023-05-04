Download Link: https://assignmentchef.com/product/solved-cs39003-assignment3
<br>
<h1> Preamble – tinyC</h1>

This assignment follows the lexical specification of C language from the International Standard <strong>ISO/IEC 9899:1999 (E)</strong>. We choose a subset of the specification as given below, and refer to this language as tinyC and subsequently (in a later assignment) specify its grammar from the <em>Phase Structure Grammar </em>given in the C Standard.

The lexical specification quoted here is written using a precise yet compact notation typically used for writing language specifications. We first outline the notation and then present the <em>Lexical Grammar </em>that we shall work with.

<h1>2           Notation</h1>

In the convention that has been followed, syntactic categories (non-terminals) are indicated by <em>italic type</em>, and literal words and character set members (terminals) by <strong>bold type</strong>. A colon (:) following a non-terminal introduces its definition. Alternative definitions are listed on separate lines, except when prefixed by the phrase “one of”. An optional symbol is indicated by the subscript “opt”, so that the following indicates an optional expression enclosed in braces.

<em>{ expression<sub>opt </sub></em><em>}</em>

<h1>3           Lexical Grammar of tinyC</h1>

<ol>

 <li><strong>Lexical Elements </strong><em>token: keyword</em></li>

</ol>

<em>identifier constant string-literal punctuator</em>

<ol start="2">

 <li><strong>Keywords </strong><em>keyword: </em>one of</li>

</ol>

<table width="180">

 <tbody>

  <tr>

   <td width="72"><strong>break</strong></td>

   <td width="58"><strong>float</strong></td>

   <td width="50"><strong>static</strong></td>

  </tr>

  <tr>

   <td width="72"><strong>case</strong></td>

   <td width="58"><strong>for</strong></td>

   <td width="50"><strong>struct</strong></td>

  </tr>

  <tr>

   <td width="72"><strong>char</strong></td>

   <td width="58"><strong>goto</strong></td>

   <td width="50"><strong>switch</strong></td>

  </tr>

  <tr>

   <td width="72"><strong>continue</strong></td>

   <td width="58"><strong>if</strong></td>

   <td width="50"><strong>typedef</strong></td>

  </tr>

  <tr>

   <td width="72"><strong>default</strong></td>

   <td width="58"><strong>int</strong></td>

   <td width="50"><strong>union</strong></td>

  </tr>

  <tr>

   <td width="72"><strong>do</strong></td>

   <td width="58"><strong>long</strong></td>

   <td width="50"><strong>void</strong></td>

  </tr>

  <tr>

   <td width="72"><strong>double</strong></td>

   <td width="58"><strong>return</strong></td>

   <td width="50"><strong>wlile</strong></td>

  </tr>

  <tr>

   <td width="72"><strong>else</strong></td>

   <td width="58"><strong>short</strong></td>

   <td width="50"> </td>

  </tr>

  <tr>

   <td width="72"><strong>extern</strong></td>

   <td width="58"><strong>sizeof</strong></td>

   <td width="50"> </td>

  </tr>

 </tbody>

</table>

<ol start="3">

 <li><strong>Identifiers </strong><em>identifier:</em></li>

</ol>

<em>identifier-nondigit identifier identifier-nondigit identifier digit</em>

<em>identifier-nondigit: </em>one of

<table width="434">

 <tbody>

  <tr>

   <td width="211">                      <strong>      a       b       c       d         e</strong></td>

   <td width="24"><strong>f</strong></td>

   <td width="42"><strong>g</strong></td>

   <td width="28"><strong>h</strong></td>

   <td width="27"><strong>i</strong></td>

   <td width="32"><strong>j</strong></td>

   <td width="28"><strong>k</strong></td>

   <td width="27"><strong>l</strong></td>

   <td width="15"><strong>m</strong></td>

  </tr>

  <tr>

   <td width="211">                             <strong>n       o      p      q         r</strong></td>

   <td width="24"><strong>s</strong></td>

   <td width="42"><strong>t</strong></td>

   <td width="28"><strong>u</strong></td>

   <td width="27"><strong>v</strong></td>

   <td width="32"><strong>w</strong></td>

   <td width="28"><strong>x</strong></td>

   <td width="27"><strong>y</strong></td>

   <td width="15"><strong>z</strong></td>

  </tr>

  <tr>

   <td width="211">                             <strong>A      B      C      D        E</strong></td>

   <td width="24"><strong>F</strong></td>

   <td width="42"><strong>G</strong></td>

   <td width="28"><strong>H</strong></td>

   <td width="27"><strong>I</strong></td>

   <td width="32"><strong>J</strong></td>

   <td width="28"><strong>K</strong></td>

   <td width="27"><strong>L</strong></td>

   <td width="15"><strong>M</strong></td>

  </tr>

  <tr>

   <td width="211"><strong>N O             P             Q          R </strong><em>digit: </em>one of</td>

   <td width="24"><strong>S</strong></td>

   <td width="42"><strong>T</strong></td>

   <td width="28"><strong>U</strong></td>

   <td width="27"><strong>V</strong></td>

   <td width="32"><strong>W</strong></td>

   <td width="28"><strong>X</strong></td>

   <td width="27"><strong>Y</strong></td>

   <td width="15"><strong>Z</strong></td>

  </tr>

  <tr>

   <td width="211">                        <strong>0     1     2     3     4     5</strong>4. <strong>Constants </strong><em>constant: integer-constant floating-constant character-constant integer-constant: nonzero-digit integer-constant digit nonzero-digit: </em>one of</td>

   <td width="24"><strong>6</strong></td>

   <td width="42"><strong>7         8</strong></td>

   <td width="28"><strong>9</strong></td>

   <td width="27"> </td>

   <td width="32"> </td>

   <td width="28"> </td>

   <td width="27"> </td>

   <td width="15"> </td>

  </tr>

  <tr>

   <td width="211"><strong>1      2             3             4          5             6 </strong><em>floating-constant:</em></td>

   <td width="24"><strong>7</strong></td>

   <td width="42"><strong>8         9</strong></td>

   <td rowspan="2" width="28"> </td>

   <td rowspan="2" width="27"> </td>

   <td rowspan="3" width="32"> </td>

   <td rowspan="3" width="28"> </td>

   <td rowspan="3" width="27"> </td>

   <td rowspan="4" width="15"> </td>

  </tr>

  <tr>

   <td colspan="3" width="277"><em>fractional-constant exponent-part<sub>opt </sub>digit-sequence exponent-part fractional-constant:</em><em>digit-sequence<sub>opt </sub></em><strong>. </strong><em>digit-sequence digit-sequence </em><strong>. </strong><em>exponent-part:</em><strong>e </strong><em>sign<sub>opt </sub>digit-sequence</em><strong>E </strong><em>sign<sub>opt </sub>digit-sequence sign: </em>one of<strong>+      –</strong><em>digit-sequence:</em><em>digit digit-sequence digit character-constant:</em>‘ <em>c-char-sequence </em>‘ <em>c-char-sequence:</em><em>c-char c-char-sequence c-char c-char:</em></td>

  </tr>

  <tr>

   <td colspan="5" width="332">any member of the source character set except</td>

  </tr>

  <tr>

   <td colspan="8" width="420">the single-quote ‘, backslash , or new-line character <em>escape-sequence</em><em>escape-sequence: </em>one of<em></em>‘ <em></em>” <em></em><strong>? </strong><em>\</em><em></em><strong>a </strong><em></em><strong>b </strong><em></em><strong>f </strong><em></em><strong>n </strong><em></em><strong>r </strong><em></em><strong>t </strong><em></em><strong>v</strong>5. <strong>String literals </strong><em>string-literal:</em></td>

  </tr>

 </tbody>

</table>

” <em>s-char-sequence<sub>opt </sub></em>” <em>s-char-sequence:</em>

<em>s-char s-char-sequence s-char</em>

<em>s-char:</em>

any member of the source character set except the double-quote ”, backslash , or new-line character

<em>escape-sequence</em>

<ol start="6">

 <li><strong>Punctuators </strong><em>punctuator: </em>one of</li>

</ol>

[ ] ( ) { } . -&gt;

++ — &amp; * + – ~ ! / % &lt;&lt; &gt;&gt; &lt; &gt; &lt;= &gt;= == != ^ | &amp;&amp; || ? : ; …

= *= /= %= += -= &lt;&lt;= &gt;&gt;= &amp;= ^= |=

, #

<ol start="7">

 <li><strong>Comments</strong>

  <ul>

   <li><em>Multi-line Comment</em></li>

  </ul></li>

</ol>

Except within a character constant, a string literal, or a comment, the characters <strong>/* </strong>introduce a comment. The contents of such a comment are examined only to identify multibyte characters and to find the characters <strong>*/ </strong>that terminate it. Thus, <strong>/* … */ </strong>comments do not nest.

<ul>

 <li><em>Single-line Comment</em></li>

</ul>

Except within a character constant, a string literal, or a comment, the characters <strong>// </strong>introduce a comment that includes all multibyte characters up to, but not including, the next new-line character. The contents of such a comment are examined only to identify multibyte characters and to find the terminating new-line character.

<h1>4           The Assignment</h1>

<ol>

 <li>Write a flex specification for the language of tinyC using the above lexical grammar. Name of your file should be ass3 <em>roll</em>.l, which should not contain the function main().</li>

 <li>Write your main() function in a separate file ass3 <em>roll</em>.c to test your lexer.</li>

 <li>Prepare a Makefile to compile the specifications and generate the lexer.</li>

 <li>Prepare a test input file ass3 <em>roll </em>c that will test all the lexical rules that you have coded.</li>

 <li>Prepare a zip-archive with the name ass3 <em>roll</em>.zip containing all the above</li>

</ol>

files and upload to Moodle.

<h1>5           Credit Distribution</h1>

<ul>

 <li>Flex Specifications: <strong>60</strong></li>

 <li>Main function and Makefile: <strong>15 + 5 = 20</strong></li>

 <li>Test file: <strong>20</strong></li>

</ul>