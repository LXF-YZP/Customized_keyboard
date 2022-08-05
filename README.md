## 键盘简单说明

键盘主控使用的是atmega32u4-mu，这里解释一下为什么使用这个芯片，因为最开始画pcb的只会画32u4-au和32u4-mu，其中32u4-mu便宜所以选的这个。
至于更便宜的apm32芯片，仿照的stm32芯片画了一个apm32的pcb图，用于制作pad，刚打样还没有制作完成。
客制化键盘制作，pcb单模无灯，外壳树脂打印。
<!-- <details><summary>打字音在B站有分享</summary>https://www.bilibili.com/video/BV1YA4y1Z7aT?spm_id_from=333.999.0.</details> -->
轴体没有润,轴下垫没有加,夹心棉和底棉都有;
更新完qmk固件之后，支持 VIA 实时改键，全键无冲。

## 项目分支
>+ master分支： 该分支是田字68的键盘数据。
>+ alice分支：  该分支是Alice配列键盘数据。
>+ hhkb分支：该分支是hhkb配列键盘数据。  
>+ forty_arrangement分支：该分支是40配列键盘数据。  
>+ keypad_frame分支： 键盘支架。 
>+ pad分支： 数字小键盘配列数据。 
>+ seventy_three_arrangement：该分支为73配列键盘数据。
>+ sixty_eight_vim：该分支是68配列键盘数据。（方向键在最下面一排）  




## 目录结构：  
>+ bom 元器件表  
>+ case 外壳图纸  
>+ config 固件文件,支持via改键，解压kafka.zip之后，直接放到qmk的keyboards目录下就可以编译生成hex文件，或者直接使用文件夹中的hex文件  
>+ gerber 制作pcb要上传到立创的压缩文件  
>+ location_plate 配列文件  
>+ pcb pcb原理图  
>+ photo 键盘渲染图，实物图  
>+ screw 螺丝  
>+ acrylic_shell 亚克力外壳图纸

## PCB说明
>>田字68pcb文件中只有无灯无开槽的是适配了3D打印外壳的；田字68的其他pcb还没有适配外壳，其实适配外壳也很简单，无灯的pcb直接修改一下外壳的type-c口即可，有灯的pcb需要在方向键上方开一个适当大小的铭牌口即可。最后解释一下为什么田字68要画这么多pcb的原因，有以下几个原因，pcb开槽和不开槽在手感上有很大差别的，开槽的会更加软弹，不开槽的手感会偏硬一点，gasket结构配上开槽pcb会更加软弹，至于pcb横开槽和全开槽在手感方面也有一点区别，所以制作了多个pcb，本人对轴灯无感，一是光污染（尤其晚上关灯之后），二是画pcb电路图很麻烦（画过一次再也不想画了，玩亚克力的可能会喜欢轴灯），但是本人对氛围灯很有好感，所以有开槽的pcb都有氛围灯。

## 配列图

##### 68配列
+ master分支的68配列如下图所示：
![image](https://github.com/LXF-YZP/Customized_keyboard/blob/master/photo/68%E9%85%8D%E5%88%97.png)

+ 下列68配列为个人的一些改动：
该配列的配套pcb和外壳还未画好，不过后期都会更新好；
七月三十号pcb外壳已更新，亚克力外壳的准备文件也已更新，亚克力外壳就不再画完整的了，可以在我更新的准备文件基础上进行修改。现在只有固件是没有更新了。如果后续我单板的话，回去更新固件，或者你单板了，可以找我要固件；
![image](https://github.com/LXF-YZP/Customized_keyboard/blob/master/photo/68vim%E9%85%8D%E5%88%97.png)


##### hhkb配列
+ hhkb分支的配列如下图：
![image](https://github.com/LXF-YZP/Customized_keyboard/blob/master/photo/hhkb.png)

+ 下列类hhkb配列为个人的一些改动：
![image](https://github.com/LXF-YZP/Customized_keyboard/blob/master/photo/hhkbvim.png)
>> 以上两个配列共用一套pcb和外壳而且已经画好上传到相关文件夹中；pcb是包含两个pcb的gerber文件的，一个是未开槽的pcb只是类hhkb配列的；一个是已经开槽的pcb，这个pcb就是上面说的兼容两个配列的pcb，而且是分离小板的；

##### Alice配列
+ 下面配列是Alice配列：
![image](https://github.com/LXF-YZP/Customized_keyboard/blob/master/photo/Alice.png)

##### 40配列

+ 40配列如下图
![image](https://github.com/LXF-YZP/Customized_keyboard/blob/master/photo/40%E9%85%8D%E5%88%97.png)

+ 下列40配列为个人的一些改动：
![image](https://github.com/LXF-YZP/Customized_keyboard/blob/master/photo/40vim%E9%85%8D%E5%88%97.png)
>> 以上两个配列共用一套pcb和外壳而且已经画好上传到相关文件夹中；

##### 73配列

+ 这里多说两句，这个配列最初是在B站看到别人发的一个pcb动态，第一眼感觉很惊艳，所以就自己设计了一款，设计的初衷是送一个朋友的，所以pcb设计的时候走线规整了很多，看着还是比较好看的，由于自己打板子的时候没有选择沉金，所以走线得仔细看才能看出好不好看，要是用沉金的话，就可以把走线都体现出来了，奈何沉金太贵了，要是开团的话选沉金还是不错的。

![image](https://github.com/LXF-YZP/Customized_keyboard/blob/master/photo/73%E9%85%8D%E5%88%97.png)

>> 这个配列开源的pcb和外壳还有固件都是自己最初设计的一版，实际送朋友的那一版pcb会开源，但是外壳不会开源，因为送朋友的外壳有很多是她自己喜欢的一些元素，所以不开源外壳。但是我有时间会再设计一款外壳。73配列带底灯版本外壳已更新，相关文件后缀带有底灯字样。

田字68全开槽不带分离小板的外壳已经更新，在case文件夹里面的case/田字68底壳.stl文件，其他部分的stl文件是通用的；固件在config/tiankafka_via.hex, via文件在config/tian_kafka_via.json
目前40配列和hhkb兼容配列的固件还没有编写，Alice配列的外壳还没有画。alice 配列图纸画好之后会上传；


##### pad

+ pad如下图

![image](https://github.com/LXF-YZP/Customized_keyboard/blob/master/photo/pad.png)

pad使用的芯片为stm32f103,可以使用apm替代，该pad为了验证芯片电路图是否使用正确所画，当前状态为未打板，建议等我打板验证之后再使用。
