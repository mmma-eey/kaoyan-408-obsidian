# CISC与RISC

返回 [[第四章 指令系统]]。来源：[[第四章原图与识别说明#原图13|原图13]]。

## 设计倾向
CISC强调较丰富的指令语义与寻址形式；RISC强调较规整的编码和寄存器运算，常采用Load/Store访问内存。x86是常见CISC例子，Arm/RISC-V常作为RISC例子。

照片中的对比表适合记忆历史设计倾向，不宜逐项写成现代处理器的硬性定义：
- RISC不等于指令一定少于100条，CISC也不能由“大于200条”定义。
- RISC不保证全部指令一周期，乘除、访存延迟等可以多周期。
- RISC不保证所有编码都同长，例如RISC-V压缩扩展有16位编码；Arm Thumb可同时有16/32位编码。
- RISC不等于“一条指令对应一套独立电路”，控制方式与ISA风格不一一对应。
- CISC可以采用流水线、并行和内部微操作，RISC也不意味着一定更低功耗或更快。

## 微程序与硬布线
复杂指令可以通过微程序或内部多步实现；简单指令常易于硬布线控制，但不能说每种CISC都只用微程序、每种RISC都只用硬布线。

“80—20规律”是照片中的经验性设计动机，应理解为常见程序对指令使用频率不均匀，不能作为固定普遍统计数字。

实际程序性能仍需综合动态指令数、CPI、频率和存储行为；见 [[计算机性能指标]]。

参考：[RISC-V官方介绍](https://docs.riscv.org/reference/isa/v20240411/unpriv/intro.html)、[Arm官方Thumb说明](https://support.arm.com/documentation/dui0379/g/Overview-of-the-ARM-Architecture/ARM--Thumb--and-ThumbEE-instruction-sets)。

关联：[[指令格式与地址数]]、[[软件语言与系统层次]]。
