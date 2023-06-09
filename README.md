# BTL_CSDL
	Hệ thông bơm nước 
Khi độ ẩm đất (H.G) < H.G_min thì máy bơm nước lên, bơm đến khi H.G = H.G_max máy dừng hoạt động
H.G_min và H.G_max là hai ngưỡng độ ẩm của cây có thể chịu được 
Ta có biểu thức Bolean:
¯(¯A  (B+¯S) )=S
Với A = 0 khi H.G < H.G_max
       B = 0 khi H.G > H.G_min
       S là trạng thái của máy bơm, S = 0 bơm, S = 1 ngắt
	Hệ thống kéo rèm tự động
L_max (ngưỡng ánh sáng max)
L_min (ngưỡng ánh sáng min)

Khi L < L_min mà rèm đang trạng thái đóng thì sẽ mở lên
Khi L > L_max mà rèm đang mở sẽ được đóng lại
Khi L < L_min mà T(time ) > 19h thì rèm cũng sẽ không mở 
S1= ¯(A ) ¯T  S1+S1 ¯S2+ ¯T  B ¯S2
S2 = S1 ¯S2  U+S1 S2 ( ¯A+ ¯B+T+ ¯D  )

Với S1 S2= 10 thì UP đi lên 
	S1 S2 = 01 đi xuống
	A = 1 (L > L max)
	B = 1 (L < L min)
	T = 1 (nút điều khiển trạng thái sử dụng) khi rèm đang ở trên mà muốn hạ xuống theo ý mình thì nhấn nút, sau khi rèm được hạ xuống thì ánh sáng thay đổi như nào cũng không làm rèm đi lên .
	U và D là trạng thái của hiện tại của rèm 
	UD = 10 rèm đang đi lên 
	UD = 01 rèm đang đi xuống
	UD = 11 rèm ở trên đã được kéo
	UD = 00 rèm ở dưới đã được hạ

	Hệ thống tăng giảm độ ẩm không khí
H_max (ngưỡng độ ẩm max mà cây chịu)
H_min (ngưỡng độ ẩm min mà cây chịu)
Htb (độ ẩm ổn định nhất cho cây)

Khi H < H_min máy phun sương hoạt động đến khi H = Htb thì dừng
Khi H > H_max quạt hút hoạt động 
đến khi H = Htb thì dừng
Ta có biểu thức Bolean
	Quạt hút (S1 = 0 hoạt động )
¯(¯B  ¯C  S2 (¯A+¯S1))=S1 
	Phun Sương (S2 = 0 hoạt động)
¯(¯A  S1 ¯C  (B+¯S2))=S2
A = 1, H > H_max 
B = 1, H < H_min
C =1, H = Htb  

	Hệ thống tăng, giảm nhiệt độ 
C_max (nhiệt đỗ cao nhất cây chịu được)
C_min (nhiệt độ thấp nhất cây chịu được)
C_tb (nhiệt độ ổn định cây phát triển tốt)
Khi C < C_min sò nóng hoạt động đến khi C = C_tb thì dừng
Khi C > C_max quạt mát hoạt động 
đến khi C = Ctb thì dừng

Ta có biểu thức Boolean
	Quạt mát (S1 = 0 hoạt động )
¯(¯B  ¯C  S2 (¯A+¯S1))=S1 
	Sò nóng (S2 = 0 hoạt động)
¯(¯A  S1 ¯C  (B+¯S2))=S2
A = 1, C > C_max 
B = 1, C < C_min
C =1, C = C_tb  

