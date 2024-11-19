AST（抽象语法树）: https://zhuanlan.zhihu.com/p/51174224  

fsm:似乎就是本科学的状态转换  

**yosys内文件说明：**
kernel/：包含 Yosys 的核心框架代码。  
passes/：实现了逻辑综合、优化、技术映射等功能的具体逻辑。  
frontends/：实现对 Verilog、BLIF 等输入文件格式的解析。  
backends/：实现将综合后的设计导出为不同的格式（如 Verilog、EDIF）。  
tests/：包含测试用例。  
Makefile：用于构建整个项目。  