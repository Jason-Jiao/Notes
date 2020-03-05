## 多线程的作用
运行以下两个代码段，感受区别
```python
#coding=utf-8
import time

def greet(index):
    print '人生苦短，我用Python!-%d' % index
    time.sleep(0.5)
    
def line_run():
    for i in range(5):
        greet(i)

if __name__ == "__main__":#入口函数的判断
    line_run()

```
```python
#coding=utf-8
import time
import threading
def greet(index):
    print '人生苦短，我用Python!-%d'%index
    time.sleep(0.5)

def async_run():
    for i in range(5):
        th = threading.Thread(target=greet,args=[i])#target指的函数名args为参数
        th.start()

if __name__ == "__main__":
    async_run()
```

```python
#检查有几个在运行的线程
print(threading.active_count)
#当前运行所有线程的名字
print(threading.enumerate())
#打印当前运行的线程
print(threading.current_thread)
#添加线程
add_thread = threading.Thread(target=函数名)
#开始线程
add_thread.start()
#堵塞主线程
add_thread.join()
```
>解释：多线程是同时都在运行，添加的线程和主线程同时运行，如果想添加的线程先运行完，再运行主线程，就用到了join()

## 更多的线程

```python
threads= [] #定义一个线程池
th1 = threading.Thread(target=函数名,args=参数，name=给线程的名字)#建立一个线程并且赋给th1，target指的函数名args为参数
#参数的形式是一个元组
threads.append(th1)#把th1线程装到threads线程池里
th2 = threading.Thread(target=xiancheng2)#target指的函数名
threads.append(th2)
for t in threads:#遍历线程池
    t.start()#开启线程
t.join()
```
## 多线程详解
>不会使时间成倍的减少，因为python每次只能运行一个线程，但是是每个线程穿插着进行，当有些不需要运行（其他地方工作时）这段时间就分配给了其他的线程，这样实现的多线程

## lock
这个是因为上面提到的python处理机制，导致有可能，数据混乱，（如两个线程同时改变同一个对象时，就可能出现意外）此时，需要使两个线程互不打扰，用到lock
```python
lock.acqire()
代码段
lock.release()
```
