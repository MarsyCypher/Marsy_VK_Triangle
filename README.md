
# VK Triangle

By Marsy 
![Logo](https://img.sanishtech.com/u/1d18443c0842b5dd9a9e39a482c7eb2a.png)


## Installation

Install my-project with npm

```bash
  npm install https://github.com/MarsyCypher/Marsy_VK_Triangle
  cd Marsy_VK_Triangle
```
    
## Versions 

1.0 Sad Release (Gold)
https://github.com/MarsyCypher/Marsy_VK_Triangle/releases/tag/Gold
## Functions 

The executable in the current state only opens a window, with a name and crashes, as shaders could not be compiled. 

The objective of the program was to make a program that generates a triangle with all possible colors, drawing a frame 60 times per second. All the steps for this are set in place and developped, but an error related to shaders prevented the program to be finished. 
## Scheme of dependencies

![Scheme](https://img.sanishtech.com/u/55e045f2cf474d6af51edcc88ce7ed5a.png)
## Checklist

![check](https://img.sanishtech.com/u/6e421624ae9d725883c03a34d0c57999.png)

### Limits of the project
This project is unfinished and not polished, as many technocal errors were encountered.
The program in the current state only opens a window with the name, but crashes and does not show geometry. Main limit and obstacle encountered was Shader module creation and compiling of the shaders folder and slang file. Compiling the shaders was not possible, which prevented the project from being finished in time. 
## Demonstration of the code

The code of the program is divided in several cpp files (with headers accordingly).

1. Renderer.cpp

This is the largest file that contains most of the steps and functions for the program. 
It puts in place all the steps needed  to generate frames for the window to draw a triangle. 

It creates the instance with technical information, then sets in place validation layers, checks and security measure that make sure that all files are in place and that there are no errors, sending a "runtime_error" in case some of the extensions are missing. 

Then it sets up a debug messenger, using debug tools to help if bugs or errors are encountered in Debug version. 

The program searches for and chooses a Physical device and a Logical device. All GPUs of the computer are put in queues and verified for their compatibility with the program. Physical device selected connects the program with the most suitable GPU, after verifying it. Logical device is more of a virtual interface that allows the code to interact with selected GPU. 

Next a swapchain and Graphics Pipeline are created, which allow the image to be generated every frame, setting in place multiple steps and buffers, including shaders (the step that blocked me and I couldn't arrive to the end).

2. Application.cpp

After setting all the steps and initializing the program and security measures, application.cpp assembles all the created large functions in a smooth and easily read code for the final main to run. 

In Init(), all previous steps are set in motion, then the program passes to Run(), which repeats the process of drawing a Frame until the program stops. When the program is terminated, it cleans the code up to avoid and memory leaks or unnecessary ressources/memory occupied.

3. VK Triangle blyat.cpp
Main file that contains contains only the int main() function, to initialize, run and destroy the program.

4. Renderer.h / Application.h / Dependencies.h / + VK includes

Header files contain announcement of variables and functions needed for cpp files to run. 

![zaebalas](https://img.sanishtech.com/u/90d79456f2406acbd99c4836bab5a077.png)
>я заебалась