## 键盘简单说明

键盘主控使用的是atmega32u4-mu，这里解释一下为什么使用这个芯片，因为最开始画pcb的只会话32u4-au和32u4-mu，其中32u4-mu便宜所以选的这个。
至于更便宜的apm32芯片，当时初学不会画，网上没有教程，后来仿照的stm32芯片画了一个apm32的pcb图，但是没有打样，所以没有把原理图放出来；还有一个原因是32u4的qmk固件编写网上教程比较多，容易编写，个人玩键盘的话没必要非用apm32芯片，如果是想学会之后开团的话，可以学习一下apm32芯片降低pcb的成本；
客制化键盘制作，pcb单模无灯，外壳树脂打印
<!-- <details><summary>打字音在B站有分享</summary>https://www.bilibili.com/video/BV1YA4y1Z7aT?spm_id_from=333.999.0.</details> -->
轴体没有润,轴下垫没有加,夹心棉和底棉都有;
更新完qmk固件之后，支持 VIA 实时改键，全键无冲。

>>项目目前有三个分支，一个是master分支，该分支是田字68的键盘数据。
>>另外一个分支是alice分支，该分支是Alice配列键盘数据。
>>还有一个分支是hhkb分支，Alice和hhkb分支pcb已经画好了，也打样了，但是外壳还没有画好，因为还没看到一个喜欢的类型，Alice和hhkb外壳后续会补充完整，后续还会不定时更新各个配列键盘的外壳。

## 目录结构：  
>+ bom 元器件表  
>+ case 外壳图纸  
>+ config 固件文件,支持via改键，解压kafka.zip之后，直接放到qmk的keyboards目录下就可以编译生成hex文件，或者直接使用文件夹中的hex文件  
>+ gerber 制作pcb要上传到立创的压缩文件  
>+ location_plate 配列文件  
>+ pcb pcb原理图  
>+ photo 键盘渲染图，真实图  
>+ screw 螺丝  
>+ acrylic_shell 亚克力外壳图纸

## PCB说明
>>田字68pcb文件中只有无灯无开槽的是适配了3D打印外壳和亚克力堆叠外壳的；田字68的其他pcb还没有适配外壳，其实适配外壳也很简单，无灯的pcb直接修改一下外壳的type-c口即可，有灯的pcb需要在方向键上方开一个适当大小的铭牌口即可。最后解释一下为什么田字68要画这么多pcb的原因，有以下几个原因，pcb开槽和不开槽在手感上有很大差别的，开槽的会更加软弹，不开槽的手感会偏硬一点，gasket结构配上开槽pcb会更加软弹，至于pcb横开槽和全开槽在手感方面也有区别，所以制作了多个pcb，本人对轴灯无感，一是光污染（尤其晚上关灯之后），二是画pcb电路图很麻烦（画过一次再也不想画了，玩亚克力的可能会喜欢轴灯），但是本人对氛围灯很有好感，所以有开槽的pcb都有氛围灯。

## 配列图

##### 68配列
+ master分支的68配列如下图所示：
![image](https://github.com/LXF-YZP/Customized_keyboard/blob/master/photo/68%E9%85%8D%E5%88%97.png)

+ 下列68配列为个人的一些改动：
该配列的配套pcb和外壳还未画好，不过后期都会更新好；
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