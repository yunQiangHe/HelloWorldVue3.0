# [vue3.0从0到1实战电商管理系统](https://juejin.im/post/5eae5d92e51d451b2e03255c#heading-0)

## yarn

## 浅谈vue3.0
- (0) 使用 ES2015 Proxy 作为其观察者机制。 这消除了以前存在的警告，使速度加倍，并节省了一半的内存开销
- (1) 重写了虚拟Dom、diff算法优化
- (2) update性能提高1.3~2倍、SSR速度提高了2~3倍
- (3) 生命周期的改变，API 通过命名导出、可以按需导入生命周期函数
- (4) 更直观的代码复用实现方式(hooks)
- (5) 更友好且更耦合的数据通信方式(provide & inject)
- (6) API 通过命名导出,更好的支持Tree Shaking
- (7) 新的更新策略： block tree（区分动态节点和静态节点）
- (8) 更好地支持typescript
