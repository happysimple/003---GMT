# 问题应对系列

## 1.字体平移

```{note}
使用-D选项
```

````bash
echo 0 140 2008-2009| gmt text -F+f10p -N  -D2.6c/0c
````

## 2.文字超出图幅

```{note}
使用-X选项
```

````bash
gmt subplot begin 4x4 -Fs4c/2.4c -M0.5c -SCb -SRl  -R-180/180/-90/90 -JX4c/2.4c -Xr20c
````

## 3.书写带有上下标的文字

```bash
@+    打开/关闭上标
@-    打开/关闭下标
```

## 4.对nc文件执行数学运算

````bash
# 两个nc文件相减（A-B）
gmt grdmath A.nc B.nc SUB = 01.nc

# 乘法
gmt grdmath A.nc 0.00001 MUL = 01.nc
````

