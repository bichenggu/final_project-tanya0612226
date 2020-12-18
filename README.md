# final_project-tanya0612226

# dice game

我做的project為:

   彼得有九個四面體骰子, 每個骰子上有數字 1–4. 科林有六個立方體骰子, 每個骰子上有數字 1–6.

   兩個人各自丟自己的骰子, 並算其總和, 總和高者贏, 若總和相同則為平局.

  Goal:彼得贏的機率、兩人平手的機率、彼得輸的機率(數字四捨五入至小數點後第七位)

做法:

1. 首先對於兩人的骰子先分開討論

      (1)將彼得的九個四面骰結果當作一個樣本空間，其大小為4的9次方

        此樣本空間中的事件為，骰到點數加總為9、10、11...36的情況，共有28種事件

        因此對於每種事件發生的次數，以(x^1+x^2+x^3+x^4)^9做展開運算

        則每種次方前的係數即為該點數總和發生的次數，將這些事件發生的次數加總後，與樣本空間的大小吻合

      (2)科林六個六面捨也同理，其結果當作一個樣本空間，大小為6的6次方

        此樣本空間中的事件為，骰到點數加總為6、7、8、9、10、11...36的情況，共有31種事件

        因此對於每種事件發生的次數，以(x^1+x^2+x^3+x^4+x^5+x^6)^6做展開運算

        則每種次方前的係數即為該點數總和發生的次數，將這些事件發生的次數加總後，與樣本空間的大小吻合

  
  
2. 再來看兩人比點數的實驗

      這個實驗中的樣本空間大小為 4^9 x 6^6

      而此樣本空間中的事件為，彼得贏、兩人平手、彼得輸，共3種事件

      將這三種事件分開討論，並求出個別事件發生的次數

      (1)彼得贏的次數

        彼得贏的情況為，其骰出的點數總和比科林高的情況

        因此將彼得骰出的28種點數事件分別做討論

        ex:彼得骰出9時，科林骰出6、7、8，即彼得獲勝，計算方法為: 彼得骰出9事件的次數，乘上科林骰出9以下事件的次數

        將此28種結果相加後，即為彼得贏的次數

      (2)兩人平手的次數

        兩人平手的情況為，兩人骰出的點數總和相等的情況

        因為彼得與柯林只有在骰出點數9、10、11...36時才有可能點數總和相等，因此只對這28種情況做討論

        ex:彼得骰出18時，科林骰出18即兩人平手，計算方法為: 彼得骰出18事件的次數，乘上科林骰出18以下事件的次數

        將此28種結果相加後，即為兩人平手的次數

      (3)彼得輸的次數

        彼得輸的情況為，其骰出的點數總和比科林高的情況

        因為彼得骰出36時不會有輸的情況發生，因此只對扣除這個結果後的這27種情況做討論

        ex:彼得骰出33時，科林骰出34、35、36，即彼得輸，計算方法為: 彼得骰出33事件的次數，乘上科林骰出33以上事件的次數

        將此27種結果相加後，即為彼得輸的次數
  
  
  
      在算出三種事件的發生次數後加總，發現其值與樣本空間大小吻合
  
  3. 最後來算彼得贏的機率、兩人平手的機率、彼得輸的機率
  
      機率的算法為，事件發生次數除以樣本空間大小

      因此將2.中算出的結果分別除以樣本空間大小後，即可得出三種事件的機率


結果:

 * 彼得獲勝的機率為 57.3144077%
 
 * 兩人平手的機率為 7.076617%
 
 * 彼得輸的機率為 35.6089753%
