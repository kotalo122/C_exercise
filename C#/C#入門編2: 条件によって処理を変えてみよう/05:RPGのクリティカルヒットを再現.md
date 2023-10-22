このチャプターでは、これまで覚えたif文による条件分岐とRandomクラスを使って、
RPGの戦闘シーンに出てくるようなクリティカルヒットをメッセージとして表示します。

if - else if - else文の基本形

// if文による条件分岐　else if
using System;
public class Program{
    public static void Main(){
        var number = 1;
        if (条件式1) {
            // 条件式1が成立したときの処理
        } else if (条件式2) {
            // 条件式2が成立したときの処理
        } else {
            // 条件式がどれも成立しなかったときの処理
        }
    }
}


比較演算子の種類
利用例	      意味	               真になる例
a < b	       a が b よりも小さい	  10 < 15
a > b	       a が b よりも大きい	  10 > 7
a <= b	     a が b 以下である	    10 <= 15
a >= b	     a が b 以上である	    10 >= 7
a != b	     a と b が等しくない	  10 != 1


``` C#
// RPGのクリティカルヒットを再現
// 比較演算子 == > < >= <= !=

// スライムと戦っている。
// 1から10のサイコロをふって、
// 6未満：サイコロの目だけダメージを与えたと表示。
// 6以上：クリティカルヒットとして、100のダメージを与えたと表示。
using System;
public class Program{
    public static void Main(){
        var random = new Random();
        var hit = random.Next(1,11);
        Console.WriteLine(hit);
        if(hit < 6) {
            Console.WriteLine("スライムに" + hit + "のダメージを与えた！");
        } else {
            Console.WriteLine("クリティカルヒット！スライムに１００のダメージを与えた");
        }
    }
}

```