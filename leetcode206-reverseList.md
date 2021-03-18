# [leetcode206：反转链表](https://leetcode-cn.com/problems/reverse-linked-list/)

# [链表的基础知识](http://c.biancheng.net/view/1570.html)

# [解题思路](https://blog.csdn.net/qq_42351880/article/details/88637387)


class Solution {    
public:     
    ListNode* reverseList(ListNode* head) {  //定义一个返回值为ListNode型的函数，函数参数为ListNode型的指针     
        
        ListNode* NewHead = nullptr; //定义一个初始为空的指向ListNode型的指针，这个指针将作为新链表的头结点    
        ListNode* node;  //中转结点 
        
        while(head != nullptr){  //判断是否为空结点，即是否到了链表尾       
            
            //旧链表头删     
            node = head;     
            head = head->next;     
            
            //头插新结点    
            node->next = NewHead;    
            NewHead = node;    
        }
        
        return NewHead;       
    }     
};
