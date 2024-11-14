#### yosys使用：

read_verilog ***.v; proc; techmap; dfflibmap -liberty *.lib; abc -nocleanup -showtmp -liberty *.v -exe also的路径 -scrpit also的脚本（不包括read和write）;write_blif *.blif

修改：    yosys/passes/techmap/abc.cc

1.将之前abc的read和write修改，因为also需要同构有-

2.因为abc能识别source，also不行，所以我这里强行输入固定命令了

3.write，also需要-x或者-l等

4.使用abc时-s -f，而also则只需要-f

5.识别，module名称，netlist改为了top

6.log_error会终止进程。所以改成了log

#### 截图如下

![image-20211031143505792](C:\Users\foggy\AppData\Roaming\Typora\typora-user-images\image-20211031143505792.png)

![image-20211031143518303](C:\Users\foggy\AppData\Roaming\Typora\typora-user-images\image-20211031143518303.png)

![image-20211031143534179](C:\Users\foggy\AppData\Roaming\Typora\typora-user-images\image-20211031143534179.png)