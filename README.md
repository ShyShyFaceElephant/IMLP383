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
# np.array屬性
- dtype 元素資料型態
- size 陣列大小
- shape NxM
- itemsize 元素占用位元組
- ndim 維度
- nbytes 總占用位元組
