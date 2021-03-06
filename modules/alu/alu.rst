==================
运算器设计
==================


输入和输出
----------

输入
^^^^

* 运算数1, 运算数2: 各16比特 (浮点数为IEEE 754, binary 16, 半精度浮动小数点数)
* 操作码: 4比特, 允许16种运算

输出
^^^^

* 运算结果: 16比特
* 溢出和出错标志: 1比特

指令集合的设计
--------------

算术逻辑运算
^^^^^^^^^^^^

* **0000** 按位与
* **0001** 按位或
* **0010** 按位异或
* **0011** 按位非(忽略运算数2)

补码整数运算
^^^^^^^^^^^^

* **0100** 补码加法
* **0101** 补码减法
* **0110** 补码乘法

..
    * **0111** 补码除法

移位运算
^^^^^^^^

* **1000** 逻辑左移
* **1001** 逻辑右移
* **1010** 算术左移
* **1011** 算术右移

浮点运算（未实现）
^^^^^^^^^^^^^^^^^^

* **1100** 浮点加法
* **1101** 浮点减法
* **1110** 浮点乘法
* **1111** 浮点除法
