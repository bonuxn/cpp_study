
## C++ のオブジェクト思考の概念を理解する

### クラスカプセル化と可視性とは

クラスのインターフェースだけを公開(可視性がある)し、
クラスのその他の実装の詳細を非公開(不可視である)にする。

重要な情報をクラスの殻に閉じ込めることをクラスカプセル化という

実装方法は、アクセス属性を使用することで実現。


code
```C++
class  MyPoint {
    int x;      // 隠ぺい
    int y;      // 隠ぺい
public:       // 他のクラスに公開
    MyPoint(int n1 = 0,int n2 = 0) : x(n1), y(n2) { }
    MyPoint operator+(const MyPoint &rmp) const {
        MyPoint temp(x,y);
        temp.x += rmp.x; temp.y += rmp.y;
        return temp;
    }
    MyPoint &operator=(const MyPoint &rmp) {
    if(this == &rmp)
      return * this;

    }
    int getx() {return x;}
    int gety() {return y;}
}
```

### 関数オーバーロードと演算子オーバーロードとは

#### 関数オーバーロード

同名関数の仮引数が違えば、 関数オーバーロード を使用できる

#### 演算子オーバーロード

先ほどのcode に記載した operator+() や、operator=() は、演算子オーバーロード


### 再利用とクラスの継承とは
