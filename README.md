LCUT - Lightweight C Unit Test Framework
========================================

Recent News
-----------

 - 2013-04-02 fork a copy to https://github.com/bigwhite/lcut.git.
 - 2012-04-13 lcut 0.3.0 Released!
 - 2012-04-10 lcut 0.3.0-rc1 published!
   - add LCUT_ARG_RETURN_COUNT and LCUT_RETV_RETURN_COUNT macros.
 - 2010-12-16 lcut 0.2.0 Released!
 - 2010-10-29 lcut 0.2.0-beta1 published!
   - add mock support
 - 2010-09-30 The first verison of lcut - LCUT 0.1.0 Released.

Motivation
----------

In late 2005，the "TDD" concept was so popular and there were many strong and mature unit testing framework available 
for Java programmers, C# programmers and even python programmers, But there were few for C programmers. I have googled 
some c unit testing framework and gave me a shot, but eventually none of them made me comfortable. so I decided 
to implement a new one for my daily work and then lcut born.

Introduction
------------

lcut is short for "Lightweight C Unit Test framework". lightweight means it is very small and easy to learn&use. 
The framework is inspired by the well-known JUnit which is invented by Kent Beck.The structure of lcut could be 
illustrated as below:

    A logical Test
          |  
          |  
      +-------------+
      TS-1    ...  TS-N
      |             |  
      |             |  
    +-------+ ... +--------+
    TC-1 TC-N TC-1 TC-N
    
    TS - Test Suite，TC - Test Case

A unit test using lcut is divided into three levels: logical test, test suite and test case. A logical test contains 
several test suites and each test suite also contains several test cases. test case is the most basic and the smallest
unit in this framework. And the three-level concept is helpful for you to organize your unit testing well.

Feature list
------------

 - small and easy to learn&use
 - inspired by xUnit
 - three-level concepts to help organizing your test well and each level could have independent setup and teardown
   fixtures
 - provide mock support (inspired by cmockery)

For more information, please open and read the luct project wiki. lcut_user_guide and its Chinese version are ready 
for you.

Build
------
 - Download the source code package
 - unzip the package
 - configure->make->make install
 
if you want to compile in 64-bit mode, pass "CPPFLAGS=-m64 LDFLAGS=-m64" to configure.