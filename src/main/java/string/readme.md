# String manipulation
wiki: https://en.wikipedia.org/wiki/Category:String_manipulation_templates

## 1. String detection
<div>
    <p>
        1. 
        <a href="https://www.lintcode.com/problem/detect-capital/description">LintCode 1193</a>:  
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/main/java/string/LintCode1193.java">Answer</a>, 
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/test/java/string/LintCode1193Test.java">Test</a>
    </p>
    <p><b>Description: </b>String detection using <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/tree/master/src/main/java/bitOperation">bit wise manipulation</a>. 
    If there has upper case in the middle while the entire word are not all in upper case, return <code>False</code>. Otherwise, return <code>True</code>.</p>
</div>

## 2. String contains
Given 2 strings, decide if one string is in another string via some operations(eg. deletion, addition, subset).<br>
<div>
    <p>
        1. 
        <a href="https://www.lintcode.com/problem/delete-characters/description">LintCode 1445</a>:  
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/main/java/string/LintCode1445.java">Answer</a>, 
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/test/java/string/LintCode1445Test.java">Test</a>
    </p>
    <p><b>Description: </b>Use two pointers on each string to decide if the first string <code>s</code> can change to the second string <code>t</code>
    via deletion.</p>
</div>

## 3. String sorting
<div>
    <p>
        1. 
        <a href="https://www.lintcode.com/problem/log-sorting/description">LintCode 1380</a>:  
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/main/java/string/LintCode1380.java">Answer</a>, 
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/test/java/string/LintCode1380Test.java">Test</a>
    </p>
    <p><b>Description: </b>Use the <code>Arrays.sort()</code> to sort the string array. <b>Lambda</b> is introduced to replace the traditional <code>Comparator</code>.</p>
</div>

## 4. String reverse
<div>
    <p>
        1. 
        <a href="https://www.lintcode.com/problem/reverse-words-in-a-string/description">LintCode 53</a>:  
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/main/java/string/LintCode53.java">Answer</a>, 
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/test/java/string/LintCode53Test.java">Test</a>
    </p>
    <p><b>Description: </b><code>Stack</code> is considering used in this question. But actually use two <code>StringBuilder</code> to do the stuff. 
    <code>StringBuilder.insert(index, content)</code> is used to act as a stack.</p>
</div>

## 5. String palindrome
<div>
    <p>
        1. 
        <a href="https://www.lintcode.com/problem/longest-palindromic-substring/description">LintCode 200</a>:  
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/main/java/string/LintCode200.java">Answer</a>, 
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/test/java/string/LintCode200Test.java">Test</a>
    </p>
    <p><b>Description: </b>Iterate through each charater in string. Treat the selected charater as the mid point of palindrome. Find the maximum length of the palindrome based on the spcified charater. Return the largest one.</p>
</div>

## 6. String to fractional binary
<div>
    <p>
        1. 
        <a href="https://www.lintcode.com/problem/binary-representation/description">LintCode 180</a>:  
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/main/java/string/LintCode180.java">Answer</a>, 
        <a href="https://github.com/Tony-Hu/ShuaTi-Online.Judge.Problems.Solving/blob/master/src/test/java/string/LintCode180Test.java">Test</a>
    </p>
    <p><b>Description: </b>Separated into 2 parts:<br>
    <b>1) Integer part</b>: Collect number from String, and do division and modification(Use <code>&</code> for higher performance) in reverse order to get it's binary representation. 
    Notice that, do fractional part first in case of it returns an <code>"ERROR"</code> and thus the program calculates the integer binary in vain.<br>
    <b>2) Fractional Part</b>: Collect the number, compare with the multiplexer <code>5, 25, 125, ...</code> step by step to get the fracional part. If the fractional part is greater equal than the current multiplexer, substract the fractional part with multiplexer, and record an <code>1</code>. Otherwise, record a <code>0</code>.
    If the length of fractional part is greater than 32, and there are remainning in fractional part, it's not accurately stored in memory, return <code>"ERROR"</code>. If there are <b>all zeros</b> in fractional part, ignore the <code>.</code>.</p>
</div>