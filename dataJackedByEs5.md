### 不可避免的缺陷与解决方案

Object.defineProperty 虽然已经能够实现双向绑定了，但是他还是有缺陷的。
：
1 只能对属性进行数据劫持，所以需要深度遍历整个对象(见1，深层遍历)
2 对于数组不能监听到数据的变化(解决方案见4,对数组的原型操作，也称之为是非法入侵操作…Vue就是干的);

方案 ：  es6出现了proxy，原生支持对整个对象拦截代理(解决1)，并且支持数组;