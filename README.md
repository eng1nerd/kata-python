# kata-python
Kata is Japanese for form, as in patterns for practice. You practice the same pattern over and over until you're better at coding. Coding kata are short programs 
you can write over and over.

###  Origin
Most of these are inspired by an ancient book [BASIC is Fun](https://www.amazon.com/Basic-Fun-Computer-Problems-Children/dp/0380806061), which was a bunch of programs you could type and run on an 8 bit machine and as a by product maybe learn to write code. In retrospect, this was pretty crazy. Most of these are about as difficult as fizz-buzz, [which as we know some people can't solve](https://en.wikipedia.org/wiki/Fizz_buzz). I've been wanting to translate the code into a modern programing language since forever. Most of the problems were algebra story problems. The solved section isn't a translation of the original, coding styles are so radically different little would be salvagable from the original.

These questions are far easier than [Cracking the Coding Interview](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/0984782850/ref=pd_sbs_14_img_0?_encoding=UTF8&psc=1&refRID=JV9XCVQ6A174G137R2W2). This set of problems isn't intended to work out if you've recently graduated from a CompSci program and still remember
your algorithms and data structures classes.

### As Interview Questions
If use in an interview, or as a take home question, in my opinion, solving these kata allow you to demonstrate:

1. __Speed__. Can you solve it quickly.
2. __An ability to discuss code__. Now that we have some real code, you can discuss specifications, design and algorithm chioces with the interviewer.
3. __Aptitude__. If you can solve a simple question, no one knows if you are a good programmer. If you can't solve a simple question, it may be a bad sign. 
4. __Proxy for a portfolio__. If you know you interview poorly and can't write code with an audience, then it is imperative to do something else to demonstrate you can write code, such as putting together a portfolio of code samples that an interviewer can look and understand quickly. Developers' best code is probably locked behind non-disclosure agreements of various sorts and even if it wasn't, it sometimes so domain specific, large and mixed with other developers work that it is hard for an intervier to see what is going on.

See [scoring](scoring.MD) for how a kata can be graded.


### Kata Solving Workflow
If you want to do a kata, fork, clone and fill out the blanks in kata, kata_functiona, etc.

Run [run_tests.sh](run_tests.sh) to execute the tests. Initially they will pass, but that won't mean anything since the code under test
is just place holder code. If your apps use a lot of blocking input, you may need to update your unit tests to only call the functions
without blocking input commands.

I've started a [syntax cheat sheet](SYNTAX_CHEAT_SHEET.MD) for looking up basic language questions. If you are doing
an open book, open internet or doing the kata after consoluting a solved solution-- that will depend on what your 
motivations are. If you are practicing for whiteboarding, you won't have the internet handy.

### Layout
The kata folder holds the blanks with some boiler plate filled in. If you are solving problems, branch and put your code here!

The kata_functional, kata_oop, kata_script are for kata problems to be solved with a particular programming style.

The solved folder has all the above solved. Except the ones I haven't gotten to yet. This is where you go to cheat or compare your code after you've already solved it.

You can make these as easy or as hard as you want, I recommend over-engineering the solution, but not so much that you can't finish it.

Easy
- [count by](kata-python/blob/master/kata/count_by/main.py)
- [formulae](kata-python/blob/master/kata/formulae/main.py)
- [full name](kata-python/blob/master/kata/full_name/main.py)
- [limerick template](kata-python/blob/master/kata/limerick_template/main.py)
- [math quiz](kata-python/blob/master/kata/math_quiz/main.py)
- [never lose](kata-python/blob/master/kata/never_lose/main.py)
- [simple savings](kata-python/blob/master/kata/simple_savings/main.py)
- [split bill](kata-python/blob/master/kata/split_bill/main.py)

Medium
- [spelling game](kata-python/blob/master/kata/spelling_game/main.py)
- [never lose](kata-python/blob/master/kata/never_lose/main.py)
- [random walk](kata-python/blob/master/kata/random_walk/main.py)
- [conversation tree](kata-python/blob/master/kata/conversation_tree/main.py)
- [spelling game](kata-python/blob/master/kata/spelling_game/main.py)
- [rhymes with](kata-python/blob/master/kata/rhymes_with/main.py)
- [descendents](kata-python/blob/master/kata/descendents/main.py). This is just a generalization of the Fibonacci question.

Harder
- [build it](kata-python/blob/master/kata/build_it/main.py). This is an odd one out because a build script calls for a different knowledge base from writing a function.
- [text adventure](kata-python/blob/master/kata/text_adventure/main.py)
- [sea battle](kata-python/blob/master/kata/sea_battle/main.py)
- [life ring](kata-python/blob/master/kata/life_ring/main.py)

#### Elements of the template
- Common futures imports. Remove some friction by writing python 2/3 compatible code, at least for the easy things, like 
print, division and unicode literals
- `__init__` Your sample code is in a module
- `__module__' This allows the code to be run on python -m module_name
- `if __file__ == '__main__':` This block runs if you execute python main.py
- There is a minimal logger set up- you don't have to mix developer oriented logging and user oriented output, i.e. make 
appropriate choices about when to log and when to use print()
- There is a skeleton for a unittest. 
- The parent fodler has a run_tests.sh bash command that will run all tests in all modules in \kata\
- A build or setup.py script normally would be essential, but it introduces too many "knowledge points"

### Python Interpretor, Libraries
I'm planning to write this in python 3 with some effort to make it python 2/3 compatible.
  
I plan to make some kata specifically for psycopg, pandas, and other libraries. At the moment, the goal is for all kata to be done with just the standard library and some development dependencies such as:

- pylint
- virtualenv, pyenv and similar 


### Kata Design Workflow
I'm solving the problems first, then I copy the skeleton to the corresponding root folders.

If you want to fix bugs in my kata code, branch and modify the /solved/ folder and make pull requests.