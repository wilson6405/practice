### - Linkedlist
自我參考結構的線性集合，每個物件叫做節點(Node)，他們透過指標鏈結(Link)串起來。
```clike
struct listNode
{
    char data;
    //...
    //...
    //...
    sturct listNode *nextPtr;
}
```
- 插入節點(insert node)
    - 宣告指向新資料的指標(newPtr)，指向前一個資料的指標(previousPtr)，指向目前資料的指標(currentPtr)。
    - 判斷新節點資料記憶體位置有沒有配置成功(newPtr != NULL)
    - ...
    - (可能有其他功能例如尋找正確位置(位置排序))。
    - ...
    - 是否為第一筆節點資料
    - 新增節點資料
- 刪除節點(delete node)
    - 宣告指向前一個資料的指標(previousPtr)，指向目前資料的指標(currentPtr)，指向欲刪除資料的指標(tempPtr)。
    - 是否為第一筆資料，是就直接釋放刪除
    - 不是的話尋找欲刪除資料(while(...))
    - 找到的話判斷是否是NULL，不是的話釋放刪除。
- 串列是否為空(Empty)
    - 是的回傳TRUE，反之FALSE。
- 印出串列(print list)
    - 用while印出每個節點資料，直到NULL。

----
### - Stack
Stacl是一種有限制Linkedlist。程式只能夠用推疊的頂端加入新節點或刪除節點。這樣的堆疊稱為先進後出(FILO)的資料結構。
```clike
struct stackNode
{
	int data;
	struct stackNode *nextPtr;
};
```
- Push
    - 宣告指向新資料的指標(newPtr)。
    - 判斷新節點資料記憶體位置有沒有配置成功(newPtr != NULL)。
    - 新增資料在最上頭
- Pop
    - 指向欲刪除資料的指標(tempPtr)。
    - 刪除在最頂端的資料。
- Stack是否為空(Empty)
    - 是的回傳TRUE，反之FALSE。
- 印出Stack(print stack)
    - 用while印出每個節點資料，直到NULL。
