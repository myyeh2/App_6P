<!--    ConsoleApp6P      -->
# 精銳矩陣計算求解器(Sharp Matrix Solver, SMS)驗證  

## 儲存庫App_6J、App_6K、App_6L、App_6M、App_6P是相同的主題，都是求解齊次解(Homogeneous Solution)，僅App_6P是求解特別解(Particular Solution)，即求解yp(t)和F(t)  

一般解(General Solution)是齊次解加特別解，齊次解$y_h$有複數的情況，而特別解$y_p$都是實數  

$M \ast \ddot{y_p}(t) + C \ast \dot{y_p}(t) + K \ast y_p(t) = f(t) \qquad.\qquad.\qquad.\qquad.\qquad.\qquad(1)$

設計週期T=2秒，M、C、K矩陣已知  

$f(t) = F(t) = B_f \ast U(t) \qquad.\qquad.\qquad.\qquad.\qquad.\qquad.\qquad.\qquad.\qquad(2)$

$y_p(t) = B_0 \ast U(t) \quad.\qquad.\qquad.\qquad.\qquad.\qquad.\qquad.\qquad.\qquad.\qquad.\qquad(3)$  

$\dot{y_p}(t) = B_0 \ast \dot{U}(t) = B_0 \ast D_1 \ast U(t) \qquad.\qquad.\qquad.\qquad.\qquad.\qquad.\qquad(4)$  

$\ddot{y_p}(t) = B_0 \ast \ddot{U}(t) = B_0 \ast D_2 \ast U(t) \qquad.\qquad.\qquad.\qquad.\qquad.\qquad.\qquad(5)$  

(2)、(3)、(4)、(5)帶入（1）式得  

$M \ast B_0 \ast D_2 + C \ast B_0 \ast D_1 + K \ast B_0 = B_f \quad.\qquad.\qquad.\qquad.\qquad.\qquad(6)$

矩陣方程式(6)，雖然$D_1$、$D_2$、和$B_f$已知，仍然無法球的$B_0$，故假設$B_0$已知，可求得$B_f$，即$f(t) = B_f \ast U(t)$  

$ F(t) = B_f \ast U(t)$  

$y_p(t) = B_0 \ast U(t)$  

$B_0 =  
\begin{bmatrix}  
5 & 0 & -1 & 0 \\ 0 & 0 & 1 & 1  
\end{bmatrix} \qquad U(t) =  
\begin{bmatrix}
cos(0.1 \ast t) \\ sin(0.1 \ast t) \\ t \\ 1  
\end{bmatrix} \quad 求得 B_f 後再求得 F(t)  
$  

$y_p(t) =  B_0 \ast U(t) =
\begin{bmatrix}
5 \ast cos(0.1 \ast t) - t \\ t + 1
\end{bmatrix}
$  

$\quad$  

$\quad$  
