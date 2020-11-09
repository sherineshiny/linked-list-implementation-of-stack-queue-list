class LinkedList{
 Node head;
 static class Node{
  int data;
  Node next;
  Node(int d)
  {
    data=d;
    next=null;
   }
  }
  public void printList()
  {
    Node n=head;
    while(n!=null){
      System.out.println(n.data+" ");
      n=n.next;
      }
     }
   class QNode{
     int key;
     QNode next;
      public QNode(int key)
      {
       this.key=key;
        this.next=null;
      }
     }
     class Queue{
       QNode front,rear;
       public Queue()
       {
        this.front=this.rear=null;
       }
       void enqueue(int key)
       {
         QNode temp=new QNode(key);
         if(this.rear==null){
          this.front=this.rear=temp;
          return;
        }
        this.rear.next=temp;
        this.rear=temp;
      }
      void dequeue()
      {
        if(this.front==null)
         return;
        QNode temp=this.front;
        this.front=this.front.next;
        if(this.front==null)
           this.rear=null;
        }
      }
   class StackUsingLinkedList{
     private class Node{
        int data;
        Node link;
       }
       Node top;
       StackUsingLinkedList()
       {
         this.top=null;
        }
       public void push(int x)
       {
         Node temp=new Node();
         if(temp==null){
           System.out.println("\n heap overflow");
           return;
          }
          temp.data=x;
          temp.link=top;
          top=temp;
          }
          public boolean isEmpty()
          {
            return top==null;
            }
          public int peek()
          {
            if(!isEmpty()){
              return top.data;
              }
             else{
               System.out.println("\nstack is empty");
               return -1;
               }
             }
             public void pop()
             {
              if(top==null){
                 System.out.println("\n stack underflow");
                 return;
               }
               top=(top).link;
              }
              public void display()
              {
                if(top==null){
                 System.out.println("\n stack underflow");
                 exit(1);
               }
               else{
                 Node temp=top;
                 while(temp!=null){
                   system.out.println(temp.data);
                   temp=temp.link;
                  }
                }
              }
            }
            public class linkedlistimplementation{
               public static void main(String[] args)
               {
                 StackUsingLinkedList obj=new StackUsingLinkedList();
                 obj.push(11);
                 obj.push(22);
                 obj.push(33);
                 obj.push(44);
                 obj.display();
                 System.out.println("\n top element is ",obj.peek());
                 obj.pop();
                 obj.pop();
                 obj.display();
                 System.out.println("\n top element is ",obj.peek());
               Queue q=new Queue;
               q.enqueue(10);
               q.enqueue(20);
               q.dequeue();
               q.dequeue();
               q.enqueue(30);
               q.enqueue(40);
               q.enqueue(50);
               q.dequeue();
               System.out.println("Queue Front:"+q.front.key);
               System.out.println("Queue Rear:"+q.rear.key);
               LinkedList llist=new LinkedList();
               llist.head=new Node(1);
               Node second=new Node(2);
               Node third=new Node(3);
               llist.head.next=second;
               second.next=third;
               llist.printList();
               }
              } 
             
             
                 
                
                   
        
        
          
