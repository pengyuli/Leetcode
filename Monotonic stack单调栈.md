# Monotonic stack 单调栈

## 单调递增栈
栈顶: 右边第一个比自己小的数 r
栈顶: 左边第一个比自己小的数 l
栈顶: 一个subarray, 自己最大subarray(l-r)


适用问题:

- 左/右第一个**
- 找一个subarry, 自己最大/小

模板(递增):
```
for (int i = 0; i < nums.length; i++) {
            while (!stack.isEmpty()&&nums[stack.peek()] > nums[i]) {
                stack.pop();
            }
            stack.push(i)
        }
```

注意: 栈中存放index还是数本身, 比较符号用</>,还是 <=/>= 



