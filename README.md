# 硬件断点Hook (HardBreakPointHook)
> #### 最多四处断点
> #### 可过内存校验
### 使用方法
``` C++
HardBreakPoint::initialize();

HardBreakPoint::set_break_point(HitRole, HitRole_Hook);
HardBreakPoint::remove_break_point(HitRole);

static bool HitRole_Hook(BulletControl* ptr) {
    ptr->maxDistance = 9999.0f;
    return HardBreakPoint::call_origin(HitRole_Hook, ptr);
}
```
