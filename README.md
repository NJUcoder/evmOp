# Build and Install Z3
git clone https://github.com/Z3Prover/z3.git
cd z3
python scripts/mk_make.py
cd build
make
sudo make install

# Download and build evmOp


#How to Use
首先使用 **python chMod.py** 改变solc目录下所有版本的编译器执行权限
然后执行 **make** 生成  **evmOp** 可执行文件
  **evmOp** 使用方式如下：
**./evmOp <opType> <solFile> <contractName> <solcVersion> <solcOpEnabled> <solcOpRuns>**

其中

opType : 优化选项

> 1 : 仅进行冗余assertion优化

> 2 : 仅进行storage重复读取优化

> 3 : 同时进行以上两种优化

solFile : 待验证合约源代码文件路径

contractName : 待验证合约名

solcVersion : Solidity编译器版本

solcOpEnabled (默认为true): true or false, 表示是否开启编译器的编译优化选项

solcOpRuns (默认为200): Estimated number of contract runs for optimizer tuning.
