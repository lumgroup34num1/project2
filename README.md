# The Rho method of reduced SM3
## 1、原理
![image](https://github.com/lumgroup34num1/project2/assets/129478488/28ff15a9-05a4-46cf-a854-6950ca353577)  
因子分解很多时候并不一定要把大整数n彻底分解成为素数的乘积，而可以求出n的某个非平凡因子。  
求解大整数的一个因子是困难的，但Euclidean算法告诉我们求两个数的最大公因子是O(logn)的时间可以得到的。
我们可以利用x和x'的碰撞使用Pollard Rho算法减少求解gcd的次数。
## 2、算法核心思想
只需要求得一个碰撞即可，不一定是x<sub>i</sub>和x<sub>j</sub>,也可以是x<sub>i+δ</sub>和x<sub>j+δ</sub>，所以在找碰撞的时候，不必逐个逐个求gcd，可以跳跃着求。由此我们可以进一步改进。
## 3、运行结果
![image](https://github.com/lumgroup34num1/project2/assets/129478488/ae5f359a-f587-43c8-a5fd-ad6f88f41877)
![image](https://github.com/lumgroup34num1/project2/assets/129478488/d611f632-c45f-4f16-833e-a114bad1f350)
![image](https://github.com/lumgroup34num1/project2/assets/129478488/ae7e6d24-9c76-42af-ac36-e9fe90ece31a)
![image](https://github.com/lumgroup34num1/project2/assets/129478488/acd9036f-8ec5-4f83-893b-dc03cae173b9)
![image](https://github.com/lumgroup34num1/project2/assets/129478488/4621767d-6147-4f7f-a242-04e87211e91d)
![image](https://github.com/lumgroup34num1/project2/assets/129478488/4642aeb2-2416-49c1-826d-046b32714f2e)
## 4、结果分析
随着需求碰撞位数的增加，rho形成的环大小成指数级增加，速度以及碰撞位数比起生日攻击显著提高。
