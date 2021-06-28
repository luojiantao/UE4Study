# UE4Study
## 网络
HasAuthority();服务端返回true

###Property replicated
- C++
  1. 声明
    UROPERTY(ReplicatedUsing=Func)
  2. 定义
    UFUNCTION()
    void OnRep();
    void GetLifetimeReplicatedProps(Tarry<FLifetimeProperty>& OutLifetimeProps) const;
    
