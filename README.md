# UE4Study
## 网络
HasAuthority();服务端返回true

bReplicates = true;
### Property replicated
- C++
  1. 声明
    UROPERTY(ReplicatedUsing=Func)
  2. 定义
    UFUNCTION()
  ```c++  
    void OnRep();//服务端不会调用，客户端会调用
    
    void GetLifetimeReplicatedProps(Tarry<FLifetimeProperty>& OutLifetimeProps) const;
    {
      DOREPLIFETINE(类名称，变量名);
    }
  ```
- 蓝图
  1. 定义
    OnRep();//服务端，客户端都会调用

### Ownership 所有权（）
  - RPC 需要确定哪个客户端将执行运行于客户端的RPC
  - Actor 复制与连接相关性
  - 在涉及所有者时的Actor属性复制条件
#### 术语
  
  1. Connection :代表一个玩家连接
  2. PlayerController 
  可以追述(Owner())到playercontroller 的对象就拥有所有权

#### 操作
  1. set owner
  
    - 生成对象时，设置owner
    
    - 调用函数SetOwner
    - possess, Unpossess 
  
  
### Actor Role

#### Authority
server
拥有对actor控制权
#### Simulated Proxy
Client中的其他客户端connection
#### Autinomous Proxy
Client中的代表自己的connection
