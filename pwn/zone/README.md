# Zone
1) Overwrite size of next block
2) Allocate next block
3) When the block is freed it will go into a different zone
4) Allocate another block from different zone
5) Now you can write more than one byte since different zone thinks the size is much larger
6) Overwrite next pointer of next block to point to stack
7) Rop into a leak
8) Call system/magic gadget if that still exists

Points: 300?
  - kind of a bitch to reverse
  - but exploitation isn't that hard
    * requires reversing the allocator though