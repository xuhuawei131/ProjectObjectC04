# ProjectObjectC04

//定义一个结构体

typedef struct {

    int width;
    
    int height;
    
    int x;
    
    int y;
    
}Rectagle;

struct Rectagle1{

    int width;
    
    int height;
    
    int x;
    
    int y;
};

int main(int argc, const char * argv[]) {
    //typedef 可以重定义类型 单片机中 很多都是这样使用 定一个32位的整数
    
    typedef int int32;
    
    int32 x,y;
    
    Rectagle r1,r2;//分配4个整形大小的空间 因为这里声明了四个整形
    
    r1.height=100;//使用.访问结构体的属性
    
    r1.width=200;
    
    r2=r1;//把r1里面的数据都拷贝到r2中 但是内存还是两块独立的内存
    
    
    Rectagle* p=&r1;//p的指针类型 还是Rectagle* 类型
    
    (*p).height=100;
    
    p->width=200;//指针访问结构体里面的内存 可以使用->访问
    
    printf("Hello, World!\n");
    return 0;
}
