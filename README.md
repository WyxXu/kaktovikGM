# kaktovikGM

卡托维克是一个现代发明的因纽特计数符号系统，适用于二十进制计数。

随便做了一个字体，只是单纯测试能不能简单地实现输入，没有特别设计。因为都是二十进制，所以把玛雅的数字也放到一起了。玛雅数字算是标注，可以帮助不懂卡托维克数字是什么的人盲猜这些符号代表数字几。除了计数符号本身，只有 period "." 和  comma "," 分别作为小数点和千位分隔符，其它符号请搭配别的字体。

Free for personal and educational use. 
If you have commercial project that needs delicately designed one, contact me. I will remake it for money.


					Inupiaq Numbers(kaktovik 二十进制)  字体制作及输入机制设计
					
					kaktovik 数字由美国阿拉斯加州 kaktovik 的因纽特高中生发明
					以符合因纽特人的传统的二十进制计数习惯
					
						0 1 2 3 3 4 5 6 7 8 9 
0-9
						a b c d e f g h i j

						A-J(不区分大小写)
						
						原版基础上，底部增加玛雅计数符号
					
					unicode 为每个字符都分配了五位数码点，
					常规输入不方便，因而仿照十六进制数的
					表达将字形映射到 0-9， a-j 等二十一个字
					符上。方便日常输入。但10以上数字用字
					母键输入还是不方便（键盘上布局太分散），
					因而设计了连字替换规则，
					
					按键组合	R	q	w
						R	Q	W
					1	1r┊1+r=6	1q┊1+q=b	1q┊1+w=g
					2	2r	2q	2w
					3	3r	3q	3w
					4	4r	4q	4w
					
					* 输入时先按数字键再按字母键, 如 g g 由 1 1 和 f  f
					先输入1 1，再输入w w，即组合显示为 g，
					（左手不用移动，自然放在键盘上就能碰到 qwr 三个键）
					* 6789 (6～9) 可789.25直f接用数字键输入，但考虑到教学场合会用到先打基本字再加附标的输入方式，也增补了连字规则
					
					
					* 因纽特数字里面原先没有 0 的概念，他们在发明代表 0 的
					符号时取了一个 双手举过头顶交叉挥动的形象
					
					
					.
![image](https://github.com/WyxXu/kaktovikGM/assets/108942702/a63c3f8a-5b0e-4d60-9979-9d92b01e98b8)


Three input mode: 

* use unicode U+01D2C0 - U+01D22D3 and `ALT + X` :)
* use 0-9 and A-J or a-j， not case sensity
* use ligature, which require editing software support opentype feature
** when 1 | 2 |3 | 4 followed by r | q | w, they will combine.

English bad bad.  Try it yourself, then you will easily figure out it.
