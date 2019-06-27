##数据库连接池示例

模拟从连接池中获取、使用、释放连接的过程。客户端获取连接的过程则时等待超时模型。

- 连接池-ConnectionPool：通过构造函数初始化连接的最大上限，通过一个双向队列维护连接，
   - 调用方调用fetch方法获取连接
   - 连接使用完后使用release释放回线程池。

- 连接-Connection：java.sql.Connection只是一个接口，最终实现由数据库驱动提供方来实现。因此使用动态代理构造一个Connection。
