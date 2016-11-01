Nguyễn Xuân Anh Thư

# Báo cáo học con trỏ:

# CON TRỎ VÀ ĐỊA CHỈ

[I. Địa chỉ](diachi)

[1. Các khái niệm liên quan đến biến](khainiem)

[2. Địa chỉ của biến](diachicuabien)

[II. Con Trỏ](contro)

[1. Khái niệm con trỏ](khainiemcontro)

[2. Phân loại con trỏ](phanloai)

[3. Khai báo biến con trỏ](khaibao)

[4. Con trỏ với mảng một chiều và với mảng nhiều chiều](motchieuvanhieuchieu)

[5. Các phép toán trên con trỏ](cacpheptoan)

[III. Quy tắc sử dụng con trỏ trong các biểu thức](quytac)

[1. Tên con trỏ](tencontro)

[2. Dạng khai báo của con trỏ](khaibaocuacontro)

[IV. Quy tắc về kiểu giá trị trong khai báo](quytacvekieugiatri)

[V. Bộ định tính Const với con trỏ](dinhtinh)

<a name"diachi"></a>
## I. Địa chỉ:
  
  Địa chỉ: Dựa vào kiểu dữ liệu khi khai báo biến máy sẽ cấp phát cho biến một địa chỉ để lưu trữ biến đó trên vùng nhớ. Mỗi biến có kiểu khác nhau thì được lưu vào các địa chỉ khác nhau.
  
   <a name"khainiem"></a>
   1. Các khái niệm liên quan đến biến:
    
    - Tên biến
    
    - Kiểu biến
    
    - Gía trị của biến
    
    * Ví dụ: int ucln=10; -> int: kiểu biến; ucln: tên biến; 10: giá trị của biến
   <a name"diachicuabien"></a>
   2. Địa chỉ của biến:
   
     a. Khái niệm:
      Địa chỉ của biến là số thứ tự của byte đầu tiên trong một dãy các byte liên tiếp mà máy dành cho biến.
     
     b. Phân loại địa chỉ của biến:
     
      Địa chỉ kiểu int: hai biến kiểu int liên tiếp cách nhau 2 byte
      
      Địa chỉ kiểu float: hai biến kiểu float liên tiếp cách nhau 4 byte
      
      Địa chỉ kiểu double,.....
      
     c. Phép lấy địa chỉ của một biến:
      Phép toán `&x` cho ta địa chỉ của biến x

<a name"contro"></a>
## II. Con trỏ:

  <a name"khainiemcontro"></a>
  1. Khái niệm con trỏ:
 
   Con trỏ là một biến dùng để chứa địa chỉ. Mỗi loại địa chỉ thì có một loại con trỏ tương ứng. Trước khi sử dụng con trỏ ta phải khai báo trước khi sử dụng.
   
  <a name"phanloai"></a>
  2. Phân loại con trỏ:
   Con trỏ kiểu int dùng để chứa địa chỉ các biến kiểu int. Tương tự với float, double,....
   
  <a name"khaibao"></a>
  3. Khai báo biến con trỏ:
  
  `<Kiểu_dữ_liệu>*<tên_biến_con_trỏ>`
  
  Ví dụ: int `*p`,`*a`;
  
  <a name"motchieuvanhieuchieu"></a>
  4. Con trỏ với mảng một chiều và nhiều chiều:
  
   a. Con trỏ với mảng một chiều:
   
    Các phần tử của mảng có thể được xác định thông qua con trỏ. 
    
    Ta có khai báo :	float a[10];	
	  
    Ta có tên mảng chính là một hằng địa chỉ trỏ tới địa chỉ phần tử đầu tiên của mảng và 
    
		    a <=> &a[0]     
       
		    a+i	<=> &a[i]   
       
		    *(a+i) <=>	a[i]
       
   b. Con trỏ với mảng nhiều chiều:
    
    ` Em không hiểu :3 `
    
  <a name"cacpheptoan"></a>
  5. Các phép toán trên con trỏ:
   
   a. Phép gán: Chỉ thực hiện khi cùng kiểu. Khi sử dụng cần phải dùng phép ép kiểu.
     
     ví dụ:
      `int x; char *p; p=(char*)(&x);`
   
   b. Phép tăng giảm địa chỉ:
   
   c. Phép so sánh: dùng để so sánh các con trỏ cùng kiểu
	
<a name"quytac"></a>
## III. Quy tắc sử dụng con trỏ trong các biểu thức:
  
  <a name"tencontro"></a>
  1. Tên con trỏ: sử dụng địa chỉ chứa trong con trỏ.
   
   Ví dụ: `float a,*p; p=&a;`
  
  <a name"khaibaocuacontro"></a>
  2. Dạng khai báo của con trỏ: sử dụng giá trị lưu tại vùng nhớ mà con trỏ trỏ tới.
   
   Ví dụ:
   
         float x=5,y,z=20,*px,*pz;  
   
         px=&x; // khi đó *px = x =5
         
         pz=&z; // *py=y=10        

   Tóm lại: px, pz có kiểu là con trỏ float thì *px,*pz thuộc kiểu số thực.

<a name"quytacvekieugiatri"></a>
## IV. Quy tắc về kiểu giá trị trong khai báo:

   Mọi thành phần của cùng một khai báo(biến, phần tử mảng, hàm, con trỏ) khi xuất hiện trong biểu thức đều cho cùng một kiểu giá trị.
   
<a name"dinhtinh"></a>
## V. Bộ định tính Const với con trỏ:

   Từ khóa const có hai tác dụng:
   
    - Dùng để khai báo và khởi đầu giá trị trong các biến trong mà sau này giá trị của nó không cho phép thay đổi bởi các lệnh trong chương trình. Chúng được gọi là đối tượng hằng.
    
    - Dùng để khai báo các đối con trỏ mà trong thân hàm ta không được phép làm thay đổi  giá trị của các đối tượng được trỏ bởi các đối này.
