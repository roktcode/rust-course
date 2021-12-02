# rust-course
A notes for the Rust course i am watching

### Stack?
- a stack is automatically-allocated
- special region in memory to store variables declared in a function
- has limited size, which when exeeded, it gives stack overflow error
- each function creates it's stack frame, which makes the function scope
only accessible by the function that created the frame
- each variable i the function  should have a size known at compile time
- when function exits, it's stack frame is released

### Heap?
- a heap is manually-allocated
- a heap is a region of the memory
- limited by physical resources  of the system
- manually allocated, so  we can allocate it manually; unlike a stack, which
is  auto-allocated and de-allocated by functions
- accessible by any function, from any where in the program
- heap allocations are expensive, and should be avoided
- the main problem with heaps is fragmentation, which makes it hard for the
program to find the right space for new allocations
- allocations in the heap are de-allocated when the program ends, unless
manually de-allocated
- when allocations are not de-allocatd, they cause "memory leak"

### Smart Pointer?
- lets us make an allocation and when the function frame is gone,
it will de-allocate automatically, sor there is nor memory leak
