> 第一次作业
> 阅读下发的《Markdown参考手册》，并使用Markdown语言为暑假期间编写的程序demo撰写介绍文档`Readme.md`。要求：内容充分、排版美观，至少插入一张图片；
***
# <lable style="color:#48D1CC">学生学分绩点计算</lable>
## <lable style="color:#FFB6C1">构造函数ScorePoint()将百分制分数转换为绩点</lable>
```C++
double ScorePoint(int a) 
{ 
    if(a>=85) return 4.0;  
    else if(a>=60) return (a-60)*0.1+1.5; 
    else return 0; 
} 
```
<lable style="color:#F4A460;font-family:宋体">
1. 当百分制分数大于等于85分时，绩点4.0</br>
2. 当百分制分数小于85分大于等于60分时，分数每减少1分，绩点减少0.1</br>
3. 当百分制分数小于60分时，绩点0</lable>

## <lable style="color:#FFB6C1">主函数main()求总学分和总绩点</lable>
```C++
int main() 
{ 
    int i,n,sum;
    double psum;
    int a[100],b[100]; 
    while(scanf("%d",&n) != EOF) 
    { 
        sum = 0; 
        psum = 0; 
        for(i = 0;i < n;i++)
        { 
            scanf("%d",&a[i]); 
            sum += a[i]; 
        } 
        for(i = 0;i < n;i++)
        { 
            scanf("%d",&b[i]); 
            psum += ScorePoint(b[i]) * a[i]; 
        } 
        printf("%.2f\n",psum/sum); 
    } 
    return 0; 
} 
```
<lable style="color:#F4A460;font-family:宋体">
1. 每门学科的学分相加即为总学分</br>
2. 每门学科的学分乘以对应的绩点求和再除以总学分即为总绩点
</lable>

***
![谢谢观看](https://image.baidu.com/search/detail?ct=503316480&z=undefined&tn=baiduimagedetail&ipn=d&word=%E8%B0%A2%E8%B0%A2&step_word=&ie=utf-8&in=&cl=2&lm=-1&st=undefined&hd=undefined&latest=undefined&copyright=undefined&cs=3880186663,1184200838&os=892743914,1079206408&simid=3471062447,511773954&pn=3&rn=1&di=47520&ln=1413&fr=&fmq=1597041082588_R&fm=&ic=undefined&s=undefined&se=&sme=&tab=0&width=undefined&height=undefined&face=undefined&is=0,0&istype=0&ist=&jit=&bdtype=0&spn=0&pi=0&gsm=0&hs=2&objurl=http%3A%2F%2Fpic.baiqi008.com%2Fuploads%2Fmmkgqqhgny.jpeg&rpstart=0&rpnum=0&adpicid=0&force=undefined "谢谢观看")
<lable style="font-size:25px">~~Thanks~~</lable>