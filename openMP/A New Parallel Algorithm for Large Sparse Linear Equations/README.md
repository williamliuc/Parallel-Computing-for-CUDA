## 1.Introduction  
   This program is to solve the large sparse symmetric linear equations, in which the forward part and back part use the self-created algorithm from Shandong University Wang Dong, the algorithm name is : Double Task Scheduling Algorithm Based on Elimination Tree(DTET). The result is about 6 times higher than that of the previous iterative program without DTET algorithm. The theoretical value can be increased by about 12 times (after vectorization), I will give you a 12 times improvement on this github in the future. Part of the implementation of the DTET algorithm is mainly in the LE_SymSprsMat.cpp file and the LE_FBackwardSym.cpp file. Operating environment for the knl knit operating environment provided by intel, the processor is Xeon Phi7250 68core 16G MCDRAM 1.4GHz, compilation environment is parallel_studio_xe_2017.  
## 2.how to run  
1. To run the program using the DTET algorithm, download all the files directly under the folder, and then upload the file to the knl runtime provided by intel, use the "make" command to generate the executable test1, and then use the command "./test" can be run. Or run the program by using high bandwidth memory and the command is "numactl --membind = 1 ./test". The latter effect is better.
2. To run the original program, the original program's file under "original", Copy all the files under "original" into the current directory, and you will get the source file of the original program.  
***  
### 1.介绍
  这个程序是解大型稀疏对称线性方程组的实现，其中前推回代部分使用了来自信息工程大学的王东大佬自创的基于消去树的双重任务调度算法（以下简称DTET）来并行计算，效果比没有使用DTET算法的前推回代程序提升6倍左右，理论值可以达到12倍左右提升（向量化后），后续会给出经向量化后提升12倍的程序。实现DTET算法的部分主要在LE_SymSprsMat.cpp文件及LE_FBackwardSym.cpp文件中。运行环境为intel提供的knl运行环境，处理器为Xeon Phi7250 68core 16G MCDRAM 1.4GHz，编译环境是parallel_studio_xe_2017.  
### 2.如何运行  
1. 若要运行使用DTET算法后的程序，直接下载该文件夹下所有文件，然后将文件上传至在intel提供的knl运行环境中，使用“make”指令生成可执行文件test1，然后直接使用指令“./test”运行即可。或者通过使用高带宽内存运行程序，指令为“numactl --membind=1 ./test”。后者效果更好。
2. 若要运行原始程序，原始程序的文件在该文件夹下的original文件夹中，将该文件夹下的相应文件用original中的文件替换即得到原始程序的源文件。


