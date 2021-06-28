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
    void OnRep();//服务端不会调用，客户端会调用
    void GetLifetimeReplicatedProps(Tarry<FLifetimeProperty>& OutLifetimeProps) const;
  
- 蓝图
  1. 定义
    OnRep();//服务端，客户端都会调用
