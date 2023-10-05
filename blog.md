# caculator
A simple code for caculator by using js
# information table
| The Link Your Class |<[xinz](https://bbs.csdn.net/forums/ssynkqtd-04)> |
 
| ----------------- |--------------- |
 
| The Link of Requirement of This Assignment |<[xinz](https://bbs.csdn.net/topics/617332156) >|
 
| The Aim of This Assignment | <Realize the basic function of calculator> |
 
| MU STU ID and FZU STU ID | <21126763|832102110> |
# PSP form
 | **Personal Software Process Stages**    | Estimated Time（minutes） | Actual Time（minutes） |
 | :-------------------------------------- | :------------------------ | :--------------------- |
 | Planning                                |          5min             |        5min            |
 | • Estimate                              |          180min           |        200min          |
 | Development                             |          145min           |        150min          |
 | • Analysis                              |          100min           |        115min          |
 | • Design Spec                           |           30min           |        15min           |
 | • Design Review                         |           15min           |         15min          |
 | • Coding Standard                       |           60min           |         60min          |
 | • Design                                |           10min           |         10min          |
 | • Coding                                |           120min          |         120min         |
 | • Code Review                           |           10min           |         5min           |
 | • Test                                  |           10min           |         20min          |
 | Reporting                               |            60min          |         120min         |
 | • Test Repor                            |            10min          |         10min          |
 | • Size Measurement                      |            5min           |         5min           |
 | • Postmortem & Process Improvement Plan |            10min          |         10min          |
 | **Sum**                                 |           770min          |         860min         |
## Description of problem-solving ideas. 
Calculators need both front-end pages and back-end code to be implemented, and I considered two solutions. 
- Solution 1: Use java eclipse to implement directly, the advantage is that this is the compilation platform I am most familiar with, the disadvantage is that the style of the front end is very complex to implement. 
- Solution 2: Use JavaScript, the advantage is that the syntax is similar to JAVA, lightweight, front-end interface code implementation is simple and easy to understand. The disadvantage is never used, to learn. Based on the pros and cons of both options, I chose option two and started searching for simple JavaScript syntax in bilibili and CSDN.

## Design and implementation process. The design includes how the code is organized and the flow chart of the key functions.
![organization of my code](https://github.com/mianmian4869/MyPostImage/blob/main/codeOrganize.jpg?raw=true)
## Code description. Show the key code of the project and explain the idea.
The most important code is how to realize the function of the calculator. 
### %
The output should be 0.01 times the input
```
mod.onclick=function(){ 
        mid = Number(displays); 
        displays=mid+'%';
        result.innerHTML=mid/100; 
    }
```
### +/-
The output is the input multiplied by -1
```
bias.onclick=function(){
        mid = Number(displays); 
        displays=mid*(-1);
        result.innerHTML=mid*(-1);
    }
```
### =
The input expression can be evaluated by using the built-in evaluation function eval() 
```
    equal.onclick=function(){
        displays=eval(displays);//自带的计算函数
        result.innerHTML=displays;
    }
```
### AC
Clear all values
```
AC.onclick=function(){
        displays="";
        result.innerHTML='0';
    }
```
### .
Each number can only have one decimal point, set a Boolean value to control, by changing the Boolean value to determine whether there is already a decimal point, if there is a decimal point, can not be used.
```
    dot.onclick=function(){
        if(displays==""){
            displays+='0.'
            result.innerHTML=displays;
        }
        if(isDot==true){
            displays+='.'
            result.innerHTML=displays;
        }
        isDot=false;
    }
```
## Displaying result functions with screenshots (or gifs) and text descriptions.
### %
- input:7%
- output:0.07
![result of %](https://github.com/mianmian4869/MyPostImage/blob/main/%E7%99%BE%E5%88%86%E5%8F%B7.png?raw=true)
### +/-
- input:2
- output:-2
![result of +/-](https://github.com/mianmian4869/MyPostImage/blob/main/%E5%8F%96%E5%8F%8D.png?raw=true)
### =
- input:3 + 6.1
 ![input](https://github.com/mianmian4869/MyPostImage/blob/main/%E5%B0%8F%E6%95%B0%E7%82%B9.png?raw=true)
- output:9.1
![output](https://github.com/mianmian4869/MyPostImage/blob/main/%E7%BB%93%E6%9E%9C.png?raw=true)
### AC
![AC](https://github.com/mianmian4869/MyPostImage/blob/main/%E8%AE%A1%E7%AE%97%E5%99%A8.png?raw=true)
### .
 ![dot](https://github.com/mianmian4869/MyPostImage/blob/main/%E5%B0%8F%E6%95%B0%E7%82%B9.png?raw=true)
## Summarize this assignment.
- 1. The calculator interface: the calculator first needs a display screen, which can be divided into a separate block, and then the number and operator into a block.

- 2. Function implementation:
     - Design different click events.
     - Consider the digital case first, we first get all the digital buttons, and then give the click event, click the button can be displayed in the display screen.
     - In the case of operators, a decimal point can only occur once in a number, so we put a switch on the decimal point. Close after the execution of a click event, until the next number can continue to assign value
     - Clear keys, percent signs and other functions are relatively simple.
