Test project for basic python tools
===================================

If the pip3 is absent - install it:
sudo apt install python3-pip

Step 1:
"""""""

Let's start slow. Check what is inside Prime.py script. There should be quite wrong implementation of a function which tells us if a number prime or not. Do not worry about correctness for now. You will be able to fix it later.

Step 2:
"""""""

We want to make automatic tests of our code. But right now there is not any system for automatic testing. So let's install it and learn how to use requirements.txt. We are going to use pytest library. You can install it in two ways:

* pip install pytest
* pip install -r requirements.txt

You can always install all packets individually but if you create products for simplicity create requirements.txt file.

Step 3:
"""""""

You know, in order to test something you need... well, tests. Some basic set of them is already prepared for you. It is *test_prime_simple.py* file. Look at what is inside. Assert is a special instruction which checks if the following statement is true. Generally, if you write *assert 1==0* your program will throw an exception. But inside test files asserts used to understand if a test is passed.

Step 4:
"""""""

Run *pytest*! Or better *pytest --verbose*

It may be a little bit slow. It is because we use *time.sleep(2)*. You may comment these lines with #, if you want.

Step 5:
"""""""

You have probably noticed file prime_complex.py. It is also a file with tests. But it is not used by pytest because of the file name. So, rename it: add test\_ atthe beginning of the file name.

Step 6:
"""""""

It is clear that the Prime module is good only as an example of buggy code. But we are not gonna fix it for now. We want to automate the testing a little bit. And for that, we are gonna use Travis-ci: https://travis-ci.org/. Do not hesitate to use GitHub authntification. Next step is syncing Travis-ci with your repository and adding your project.

It would require you to add .travis.yml file in the root of your project. After that is done, git add, git push and enjoy the view of your code being tested by Travis.

Step 7:
"""""""

Now if you still have time, please fix the Prime module, and add some tests. Do not forget to remove sleeps from tests.

