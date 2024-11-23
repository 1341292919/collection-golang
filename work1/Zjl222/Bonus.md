### 切片和数组的区别
 1. 切片是对数组的一个引用，其长度是可变的.可以动态地增加或减少元素(append,delete)。切片在函数间传递时是按引用传递的，传递了底层数组的引用。切片是在堆上分配内存的，其生命周期可以超过当前函数的执行范围，且切片内部会维护一个指向底层数组的指针、切片的长度以及切片的容量。
 2. 数组的长度是固定的，在创建时就需要指定长度，且无法动态改变。数组在函数间传递时是按值传递的。数组是在栈上分配内存的，其生命周期与创建它的函数或变量相同。

### 创建切片的方式

 1. **通过数组创建切片**：
	     使用数组的一部分来创建切片，格式为`底层数组[第一个数的下标:最后一个的下标]`。
2.  **通过`make`函数创建**：
	    使用`make([]T, 长度, 容量)`来创建一个切片，其中`T`是切片的元素类型。
3.  **通过字面量直接创建**：
	    类似于数组的创建方式，但不需要指定长度，格式为`[]T{v1, v2, ..., vn}`，其中`T`是切片的元素类型，`v1, v2, ..., vn`是切片的初始元素值。

### 创建map的方式
1.  **使用`make`函数创建**：
    格式为`make(map[键的类型]值的类型, 可选的初始容量)`。
2.  **使用字面量创建**：
    格式为`map[键的类型]值的类型{key1: value1, key2: value2, ...}`，`key1: value1, key2: value2, ...`是map的初始键值对。