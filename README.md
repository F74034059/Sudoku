我的GiveQuestion用的方法有點笨，就是亂數加上原本的東西
我本來還想要加上一些方法利亂數挖空格，但是後來我的Solve寫得有點慢，所以後來就這樣了 -.-

我的ReadIn就是很普通的把輸入的東西存成一個Global 的陣列

我的Solve，首先就是先用我QuestionPreCheckNG去檢查說現在輸入的陣列是不是無解的狀況
我ocp[10]這個陣列就是去存-1跟1~9的個數，然後去檢查行宮列
如果-1的個數不是3個就會有問題，如果某個數字備用兩次甚至以上也有問題 
以上就是會造成無解的狀況，如果無解就印出0
解出答案有兩種不同的順序，一種是從前面一種是從後面
如果前後解出來答案相同代表只有唯一解，如果不同的話就是有多重解，就印出2
在解的同時，如果這個空格解不出來代表前面的格子有填錯
所以，我有一個陣列暫存步數，