C#でHTMLを出力する方法を学びます。見出しや太字などを使ってみましょう!¥

文字データの呼び名
C# プログラムでは、文字データのことを「テキスト」「文字列」(もじれつ)「String」(ストリング/ストリングス)と呼ぶことがあります。

 C# で改行したくない場合

```C#
// HTMLを表示する
using System;
public class Program{
    public static void Main(){
        Console.Write("<h1>hello world</h1>");
        Console.Write("<p>世界の皆さん、");
        Console.Write("<b>こんにちは</b></p>");
    }
}
```

```C#
// HTMLを表示する 開業したくない場合はWriteメソッド
using System;
public class Program{
    public static void Main(){
            Console.Write("<h1>hello world</h1>");
            Console.Write("<p>世界のみなさん,");
            Console.Write("<b>こんにちは</b></p>");
    }
}
```


```C#
// HTMLを表示する 改行の場合は改行したいところで<br>
// " の中に<br>"
using System;
public class Program{
    public static void Main(){
        Console.Write("<h1>hello world</h1>");
        Console.Write("<p>世界の皆さん、<br>");
        Console.Write("<b>こんにちは</b></p>");
    }
}
```