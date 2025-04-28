# cs61a-lab-10--scheme-solved
**TO GET THIS SOLUTION VISIT:** [CS61A Lab 10- Scheme Solved](https://www.ankitcodinghub.com/product/cs61a-lab-10-scheme-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;119676&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS61A  Lab 10- Scheme Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Starter Files

Download lab10.zip. Inside the archive, you will find starter files for the questions in this lab, along with a copy of the Ok autograder.

Topics

Consult this section if you need a refresher on the material for this lab. It’s okay to skip directly to the questions and refer back here should you get stuck.

Scheme

Scheme is a famous functional programming language from the 1970s. It is a dialect of Lisp (which stands for LISt Processing). The first observation most people make is the unique syntax, which uses a prefix notation and (often many) nested parentheses (see http://xkcd.com/297/). Scheme features first-class functions and optimized tail-recursion, which were relatively new features at the time.

Scheme Editor

As you’re writing your code, you can debug using the Scheme Editor. In your scheme folder you will find a new editor. To run this editor, run python3 editor. This should pop up a window in your browser; if it does not, please navigate to localhost:31415 and you should see it.

Make sure to run python3 ok in a separate tab or window so that the editor keeps running.

If you find that your code works in the online editor but not in your own interpreter, it’s possible you have a bug in code from an earlier part that you’ll have to track down. Every once in a while there’s a bug that our tests don’t catch, and if you find one you should let us know!

Expressions

Primitive Expressions

Just like in Python, atomic, or primitive, expressions in Scheme take a single step to evaluate. These include numbers, booleans, symbols.

py scm&gt; 1234 ; integer 1234 scm&gt; 123.4 ; real number 123.4

Symbols

Out of these, the symbol type is the only one we didn’t encounter in Python. A symbol acts a lot like a Python name, but not exactly. Specifically, a symbol in Scheme is also a type of value. On the other hand, in Python, names only serve as expressions; a Python expression can never evaluate to a name.

“`py scm&gt; quotient ; A name bound to a built-in procedure

[quotient]

scm&gt; ‘quotient ; An expression that evaluates to a symbol quotient scm&gt; ‘hello-world! hello-world! “`

Booleans

In Scheme, all values except the special boolean value #f are interpreted as true values (unlike Python, where there are some false-y values like 0). Our particular version of the Scheme interpreter allows you to write True and False in place of #t and #f. This is not standard.

“`py scm&gt; #t

t

scm&gt; #f f

“`

Call Expressions

Like Python, the operator in a Scheme call expression comes before all the operands. Unlike Python, the operator is included within the parentheses and the operands are separated by spaces rather than with commas. However, evaluation of a Scheme call expression follows the exact same rules as in Python:

1. Evaluate the operator. It should evaluate to a procedure.

2. Evaluate the operands, left to right.

3. Apply the procedure to the evaluated operands.

Here are some examples using built-in procedures:

“`py scm&gt; (+ 1 2) 3 scm&gt; (- 10 (/ 6 2)) 7 scm&gt; (modulo 35 4) 3 scm&gt; (even? (quotient 45 2)) t

“`

Special Forms

The operator of a special form expression is a special form. What makes a special form “special” is that they do not follow the three rules of evaluation stated in the previous section. Instead, each special form follows its own special rules for execution, such as short-circuiting before evaluating all the operands.

Some examples of special forms that we’ll study today are the if, cond, define, and lambda forms. Read their corresponding sections below to find out what their rules of evaluation are!

Control Structures

if Expressions

The if special form allows us to evaluate one of two expressions based on a predicate. It takes in two required arguments and an optional third argument: py (if &lt;predicate&gt; &lt;if-true&gt; [if-false])

The first operand is what’s known as a predicate expression in Scheme, an expression whose value is interpreted as either #t or #f.

The rules for evaluating an if special form expression are as follows: 1. Evaluate &lt;predicate&gt;.

2. If &lt;predicate&gt; evaluates to a truth-y value, evaluate and return the value if the expression &lt;if-true&gt;. Otherwise, evaluate and return the value of [if-false] if it is provided.

Can you see why this expression is a special form? Compare the rules between a regular call expression and an if expression. What is the difference?

Step 2 of evaluating call expressions requires evaluating all of the operands in order. However, an if expression will only evaluate two of its operands, the conditional expression and either &lt;true-result&gt; or &lt;false-result&gt;. Because we don’t evaluate all the operands in an if expression, it is a special form.

Let’s compare a Scheme if expression with a Python if statement:

Scheme Python

“`py scm&gt; (if (&gt; x 3) 1 2) “` “`py &gt;&gt;&gt; if x &gt; 3: … 1 … else: … 2 “`

Another difference between the two is that it’s possible to add more lines of code into the suites of the Python if statement, while a Scheme if expression expects just a single expression for each of the true result and the false result.

One final difference is that in Scheme, you cannot write elif cases. If you want to have multiple cases using the if expression, you would need multiple branched if expressions:

Scheme Python

“`py scm&gt; (if (&lt; x 0) ‘negative (if (= x 0) ‘zero ‘positive ) ) “` “`py &gt;&gt;&gt; if x &lt; 0: … ‘negative’ … else: … if x == 0: … ‘zero’ … else: … ‘positive’ “`

cond Expressions

Using nested if expressions doesn’t seem like a very practical way to take care of multiple cases. Instead, we can use the cond special form, a general conditional expression similar to a multi-clause if/elif/else conditional expression in Python. cond takes in an arbitrary number of arguments known as clauses. A clause is written as a list containing two expressions: (&lt;p&gt; &lt;e&gt;).

py (cond (&lt;p1&gt; &lt;e1&gt;) (&lt;p2&gt; &lt;e2&gt;) … (&lt;pn&gt; &lt;en&gt;) [(else &lt;else-expression&gt;)])

The first expression in each clause is a predicate. The second expression in the clause is the return expression corresponding to its predicate. The optional else clause has no predicate.

The rules of evaluation are as follows:

1. Evaluate the predicates &lt;p1&gt;, &lt;p2&gt;, …, &lt;pn&gt; in order until you reach one that evaluates to a truth-y value.

2. If you reach a predicate that evaluates to a truth-y value, evaluate and return the corresponding expression in the clause.

3. If none of the predicates are truth-y and there is an else clause, evaluate and return &lt;else-expression&gt;.

As you can see, cond is a special form because it does not evaluate its operands in their entirety; the predicates are evaluated separately from their corresponding return expression. In addition, the expression short circuits upon reaching the first predicate that evaluates to a truth-y value, leaving the remaining predicates unevaluated.

The following code is roughly equivalent (see the explanation in the if expression section):

Scheme Python

“`py scm&gt; (cond ((&gt; x 0) ‘positive) ((&lt; x 0) ‘negative) (else ‘zero)) “`py &gt;&gt;&gt; if x &gt; 0: … ‘positive’ … elif x &lt; 0: … ‘negative’ … else: … ‘zero’

“` “`

Defining Names

The special form define is used to define variables and functions in Scheme. There are two versions of the define special form. To define variables, we use the define form with the following syntax:

py (define &lt;name&gt; &lt;expression&gt;)

The rules to evaluate this expression are

1. Evaluate the &lt;expression&gt;.

2. Bind its value to the &lt;name&gt; in the current frame.

3. Return &lt;name&gt;.

The second version of define is used to define procedures:

py (define (&lt;name&gt; &lt;param1&gt; &lt;param2&gt; …) &lt;body&gt; )

To evaluate this expression:

1. Create a lambda procedure with the given parameters and &lt;body&gt;.

2. Bind the procedure to the &lt;name&gt; in the current frame.

3. Return &lt;name&gt;.

The following two expressions are equivalent:

py scm&gt; (define foo (lambda (x y) (+ x y))) foo scm&gt; (define (foo x y) (+ x y)) foo

define is a special form because its operands are not evaluated at all! For example, &lt;body&gt; is not evaluated when a procedure is defined, but rather when it is called. &lt;name&gt; and the parameter names are all names that should not be evaluated when executing this define expression.

Lambda Functions

All Scheme procedures are lambda procedures. To create a lambda procedure, we can use the lambda special form: py (lambda (&lt;param1&gt; &lt;param2&gt; …) &lt;body&gt;)

This expression will create and return a function with the given parameters and body, but it will not alter the current environment. This is very similar to a lambda expression in Python!

py scm&gt; (lambda (x y) (+ x y)) ; Returns a lambda function, but doesn’t assign it to a name (lambda (x y) (+ x

y)) scm&gt; ((lambda (x y) (+ x y)) 3 4) ; Create and call a lambda function in one line 7

Required Questions

What Would Scheme Display?

Q1: Combinations

Let’s familiarize ourselves with some built-in Scheme procedures and special forms!

Use Ok to unlock the following “What would Scheme print?” questions:

py python3 ok -q combinations -u

“`py scm&gt; (- 10 4) scm&gt; (* 7 6) scm&gt; (+ 1 2 3 4) scm&gt; (/ 8 2 2) scm&gt; (quotient 29 5) scm&gt; (modulo 29 5) “`

“`py scm&gt; (= 1 3) ; Scheme uses ‘=’ instead of ‘==’ for comparison scm&gt; (&lt; 1 3) scm&gt; (or 1 #t) ; or special form short circuits scm&gt; (and #t #f (/ 1 0)) scm&gt; (not #t) “` “`py scm&gt; (define x 3) scm&gt; x

scm&gt; (define y (+ x 4)) scm&gt; y

scm&gt; (define x (lambda (y) (* y 2))) scm&gt; (x y) “`

“`py scm&gt; (if (not (print 1)) (print 2) (print 3)) scm&gt; (* (if (&gt; 3 2) 1 2) (+ 4 5)) scm&gt; (define foo (lambda (x y z) (if x y z))) scm&gt; (foo 1 2 (print ‘hi)) scm&gt; ((lambda (a) (print ‘a)) 100) “`

Coding Questions

Q2: Over or Under

Define a procedure over-or-under which takes in a number num1 and a number num2 and returns the following:

-1 if num1 is less than num2

0 if num1 is equal to num2

1 if num1 is greater than num2

Challenge: Implement this in 2 different ways using if and cond!

py (define (over-or-under num1 num2) ‘YOUR-CODE-HERE )

Use Ok to test your code:

py python3 ok -q over_or_under

Q3: Make Adder

Write the procedure make-adder which takes in an initial number, num, and then returns a procedure. This returned procedure takes in a number inc and returns the result of num + inc.

Hint: To return a procedure, you can either return a lambda expression or define another nested procedure. Remember that Scheme will automatically return the last clause in your procedure.

You can find documentation on the syntax of lambda expressions in the 61A scheme specification!

py (define (make-adder num) ‘YOUR-CODE-HERE )

Use Ok to test your code:

py python3 ok -q make_adder

Q4: Compose

Write the procedure composed, which takes in procedures f and g and outputs a new procedure. This new procedure takes in a number x and outputs the result of calling f on g of x.

py (define (composed f g) ‘YOUR-CODE-HERE )

Use Ok to test your code:

py python3 ok -q composed

Q5: Pow

Implement a procedure pow for raising the number base to the power of a nonnegative integer exp for which the number of operations grows logarithmically, rather than linearly (the number of recursive calls should be much smaller than the input exp). For example, for (pow 2 32) should take 5 recursive calls rather than 32 recursive calls. Similarly, (pow 2 64) should take 6 recursive calls.

Hint: Consider the following observations:

1. $x^{2y} = (x^{y})^{2}$

2. $x^{2y+1} = x(x^{y})^{2}$

(define (pow base exp) ‘YOUR-CODE-HERE ) “` Use Ok to unlock and test your code: py python3 ok -q pow -u python3 ok -q pow

Submit

Make sure to submit this assignment by running:

py python3 ok –submit
