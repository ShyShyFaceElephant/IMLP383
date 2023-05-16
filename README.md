# IMLP383
## Unit 0 github教學
1. create repository
2. Add README.md 新增筆記檔
### git抓資料與上傳
1. git --version
2. cd XXX/XXX/
3. git clone https://xxxxxx
4. cd /XXX
5. git branch
6. git status
7. git add
8. git add xxx.txt
9. git commit -m "message"
10. git push

## Unit 1 丟失QQ
## Unut 2 - 1 NumPy基礎
### array vs. list
- list 資料型態可以不同
- list 可以自由增減元素
```python
lis = [2,4,5]
arr = np.array(lis)
arr += 1 #全部加一
# np.array初始化
arr=np.array(lis,dtype=float)
arr=np.arange(5) #[0,1,2,3,4]
arr=np.zeros(5) #[0,0,0,0,0]
arr=np.ones(5) #[1,1,1,1,1]
arr=np.zeros((2,2)) #[[0,0],[0,0]]
# reshape
arr=np.arange(16)
b=a.reshape((4,4)) #[[0,1,2,3],[4,5,6,7],[8,9,10,11],[12,13,14,15]]
# 亂數
seed(int) # 亂數種子
random() # 0.0 ~ 0.1 亂數
randint(min,max,size) # 亂數陣列(或整數)
rand(row,col) #亂數陣列
randn(row,col) #常態分佈亂數陣列
```
### np.array屬性
- dtype 元素資料型態
- size 陣列大小
- shape 回傳(N,M)
- itemsize 元素占用位元組
- ndim 維度
- nbytes 總占用位元組

## Unut 2 - 2 NumPy純量、向量、矩陣

```python
C = A.copy() #複製陣列
A.fill(4) #所有元素填成4
```
### 向量(一維)
```python
C = (A % 2 == 0) # 布林陣列偶數為True
C = A.dot(B) # dot運算
np.linalg.norm(V) # 向量長度
C = A[:,np.newaxis] #新增維度
C = concatenate((a,b)) #陣列連接
C = A.ceil() #向上取整
C = A.floor() #向下取整
C = np.random.randint(min,max,size)
C = np.random.rand(size) # 0~1隨機陣列
```
### 矩陣(二維)
```python
C = A + B
C = A - B
C = A * B #對應元素一一相乘
C = A / B  #對應元素一一相除
C = A.dot(B) #才是真正的矩陣相乘
C = A.ravel() #平坦化
C = A.transpose #轉置矩陣
C = concatenate((a,b),axis=0) #axis=0向下連接、axis=1向右連接
C = np.sum(A,axis=0) #縱向和結果陣列
C = np.meam(A,axis=0) #縱向平均結果陣列
C = np.average(A,axis=0,weights=w) #縱向加權平均結果陣列
C = np.var(A,axis=0) #縱向變異數結果陣列
C = np.sort(A,axis=0) #縱向排序
```
### 陣列廣播性質
- 形狀不符矩陣在做四則運算時，會自動擴充。
