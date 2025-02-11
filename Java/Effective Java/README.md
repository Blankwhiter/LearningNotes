# 1.考虑用静态工厂方法代替构造器
    不必在每次调用时都创建一个对象，可以先将对象缓存起来，需要时直接返回，避免创建不必要的重复对象。比较时可以直接用 == 操作符。
# 2.遇到多个构造器参数时要考虑构建器
  2.1 重叠构造器模式
      这个构造器通常需要许多你本不想设置的参数，但还是不得不为它们传递值。随着参数数目的增多，很快就会失去了控制。客户端代码也会很难编写，可读性也不好。
  2.2 JavaBean模式
      因为构造过程被分到了几个调用中，在构造过程中 JavaBean 可能处于不一致的状态。若试图使用处于不一致状态的对象，将会导致失败，调试起来也十分困难。程序员需要付出额外的努力来确保它的线程安全。
  2.3 Builder模式
      若类的构造器或者静态工厂中具有多个参数，设计这种类时，Builder 模式就是种不错的选择，特别是当大多数参数都是可选的时候。它较传统的重叠构造器模式相比，更易于阅读；而较 JavaBean 模式，更加安全。

# 3.通过私有构造器或枚举类实现单例属性
  3.1 公有静态成员
  3.2 静态工厂方法
  3.3 单元素枚举

# 4.通过私有构造器强化不可实例化的能力

# 5.避免创建不必要的对象  
