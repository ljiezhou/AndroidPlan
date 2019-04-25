计算一个View的最大层数：  
```
private int maxDeep2(View view) {
    if (!(view instanceof ViewGroup)) return 0;//如果不是ViewGroup，表示没有子View

    ViewGroup viewGroup = (ViewGroup) view;

    if (viewGroup.getChildCount() == 0) return 0;//同上

    int max = 0;

    for (int i = 0; i < viewGroup.getChildCount(); i++) {
        int deep = maxDeep2(viewGroup.getChildAt(i)) + 1;
        if (deep > max) max = deep;
    }

    return max;
}
```