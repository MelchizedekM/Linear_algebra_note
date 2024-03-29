# Linear Algebra 

## Chapter 1 Vector, Vector space, and Linear

欢迎来到我们线性代数课程的第一章，本章我们会从之前所学的对向量的朴素认知出发发展出什么是vector space进而延伸到对linear的思考和定义。

在我们高中的学习过程中，我们已经接触到了一种特殊的量——向量（或矢量）。在过去的学习中我们认为这种量不只有数值大小，还有方向。我们一般会将他们写成(a,b,c)的形式。例如(6,1,2)就代表着一个在x方向延伸六个单位长度，在y方向延伸一个单位长度，在z方向延伸了两个单位长度的向量。但是这种表述方式并不够规范，我们也不好表示一组有着某些抽象关系的向量，例如所有从原点发出的向量。毕竟像 $ \{(x,y,z):x\in  \mathbb{R},y\in \mathbb{R},z \in \mathbb{R} \} $ 的表达并不算简单，在我们引入更多坐标轴变量的时候也会更费墨水，因此我们想要引入一些特殊的符号来更加方便的表述这样的list（有序列）。

我们首先严谨的定义一下什么是list和list的length。
我们说n个数构成了一个length为n的list当且仅当这n个数以一种有序的方式排列在一起组合成一个元素。
我们一般将这种有序列写作 $ (x_1,x_2,x_3,…,x_n) $ 。

在此基础上，我们便可以定义在任意n下所有长度为n的list的集合了
我们定义 $ \mathbb{R}^n $ 为所有长度为n的list的集合，即
 $$ \mathbb{R}^n≔\{(x_1,x_2,x_3,…,x_n):\forall i\in \mathbb{Z} \,\, x_i\in  \mathbb{R} \} $$ 
而我们称其中的 $ x_i $ 为the i-th coordinate。

例如
 $$ \mathbb{R}^4≔\{(x_1,x_2,x_3,x_4):\forall i\in \mathbb{Z} \,\, x_i\in  \mathbb{R} \} $$ 

现在我们非常神奇地发现，我们之前所学过的所谓vector都是属于 $\mathbb{R}^2$ 或 $\mathbb{R}^3$ 的list。回忆我们曾经学过的向量的加法，比如(6,1,2)+(12,1,9)=(6+12,1+1,9+9)加法的方式就是简单的将不同coordinate上的元素分别相加。

那么类比的，我们就可以定义任意n下 $\mathbb{R}^n$ 中元素的加法：
 $$ \forall x,y\in \mathbb{R}^n,x+y∶=z \,\,\, \text{where} \,\,\, z_i=x_i+y_i  \forall i $$ 
我们可以显然的发现，这里的加法是符合交换律的，在这里我们就不做证明，留待读者自证。
再根据我们对零的一般感知，也就是所有数加0都是它本身，我们可以定义在 $\mathbb{R}^n$ 中的0:
 $$ \forall x\in \mathbb{R}^n \,\,\,  x+0=x $$ 
我们可以显然的发现在所有 $\mathbb{R}^n$ 中0都是唯一的并且0=(0,0,0,…,0)

当然，我们的数学家不愿意止步于此。我们希望将我们熟悉的欧几里得空间也就是 $\mathbb{R}^n$ 中的朴素认知拓展推广到更加抽象的一般集合中。再根据我们对vector也就是向量的朴素认知将其推广到一般集合中的一般元素。我们便有了更加抽象和一般化的对vector space和vector的定义：

我们说一个集合 $ \mathcal{V} $ 是vector space当且仅当它满足以下所有性质：
	1. Commutativity：  $\forall  u,v\in \mathcal{V} \,\, u+v=v+u$ 
	2. Associativity： $ \forall  u,v,w \in \mathcal{V} \,\, u+(v+w)=(v+u)+w \,\,\, \text{and} \,\,\, \forall  a,b\in \mathbb{R} \,\, a(bv)=(ab)v $ 
	3. Additive identity： $ \exists 0\in \mathcal{V} \,\, \forall  v\in \mathcal{V} \,\, v+0=v $ 
	4. Additive inverse： $ \forall  v\in \mathcal{V} \,\, \exists  u\in \mathcal{V} \,\, v+u=0 $ 
	5. Multiplicative identity： $ \forall  v\in \mathcal{V} \,\, 1v=v $ 
	6. Distributive properties： $ \forall  u,v\in \mathcal{V} \,\, \forall  a,b\in \mathbb{R} \,\,  a(v+u)=av+au \,\, (a+b)v=av \,\,\,  \text{and} \,\,\,  +bv $ 

而我们定义所有属于 $ \mathcal{V} $ 这个vector space的元素都是vector。

我们可以很简单的验证 $ \mathbb{R}^n $ 是一个vector space。

而我们也可以举出一些更加奇怪的vector space的例子：
如果我们定义 $ P(n) ∶=\{ \sum_{i=0}^n p_i t^i :\forall p_i\in \mathbb{R}\} $  那么我们可以发现P(n)也是一个vector space。

自然的，我们会思考，例如P(n)和\mathbb{R}^n的这些vector space之间会不会有一种内在联系呢？
显然我们会发现任意一个 $ \sum_{i=0}^n p_i t^i $ 的多项式都可以被 $ (p_1,p_2,…,p_n) $ 唯一确定的表示，我们将这种关系称为isomorphism。对于这一关系的定义完善我们先按下不表，在之后的课程中再进行介绍。


