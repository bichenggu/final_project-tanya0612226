# final_project-tanya0612226

我做的project為:

彼得有九個四面體骰子, 每個骰子上有數字 1–4. 科林有六個立方體骰子, 每個骰子上有數字 1–6.

兩個人各自丟自己的骰子, 並算其總和, 總和高者贏, 若總和相同則為平局.

Goal:彼得贏的機率、兩人平手的機率、彼得輸的機率(數字四捨五入至小數點後第七位)

做法:

1. 首先對於兩人的骰子先分開討論

將彼得的九個四面骰結果當作一個樣本空間，其大小為4的9次方

而此樣本空間中的事件為，骰到點數加總為9、10、11...36的情況

因此對於每種事件發生的次數，以<img src="https://render.githubusercontent.com/render/math?math=(x^1+x^2+x^3+x^4)^9">做展開運算
