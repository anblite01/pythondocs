第一章:数据结构
===============

1.deque
-------

1.1
~~~

from collections import deque

q=deque(maxlen=5)

q.append(5)

q.appendleft(4)

q.pop()

q.popleft()

2.heapq
-------

2.1
~~~

import heapq

nums = [1, 8, 2, 23, 7, -4, 18, 23, 42, 37, 2]

print(heapq.nlargest(3,nums))

print(heapq.nsmallest(3,nums))

portfolio = [

::

   {'name': 'IBM', 'shares': 100, 'price': 91.1},
   {'name': 'AAPL', 'shares': 50, 'price': 543.22},

]

cheap=heapq.nsmallest(3,portfolio,key=lambda s:s['price'])

expensive=heapq.nlargest(3,portfolio,key=lambda s:s['prices'])

nums = [1, 8, 2, 23, 7, -4, 18, 23, 42, 37, 2]

heap=list(nums)

heapq.heapify(heap)

heapq.heappop(heap)

2.2
~~~

优先级队列 ``backtick``

::

   import heapq
   class Pp:
       def __init__(self):
           self._queue=[]
           self._index=0

       def push(self,item,priority):
           heapq.heappush(self._queue,(-pri                        priority,self._index,item))
           self._index+=1
       def pop(self):
           return heapq.heappop(self._queue)[-1]


   class Item:
       def __init__(self,name):
           self.name=name
       def __repr__(self):
           return 'Item({!r})'.format(self.name)

   q=Pp()
   q.push(Item('foo'), 1)
   q.push(Item('bar'), 5)
   q.pop()
