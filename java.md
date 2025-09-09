# サンプルコード
## 2.3
・HelloWorld.java
```
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}
```

## 3.1.1
・Calculation.java
```
package basic.part3_1;

public class Calculation {
    public static void main(String[] args) {
        // 基本的な算術演算子
        System.out.println(5 + 2); // 足し算
        System.out.println(5 - 2); // 引き算
        System.out.println(5 * 2); // 掛け算
        System.out.println(5 / 2); // 割り算
        System.out.println(5 % 2); // 余り

        // 計算順序は数学のルールに則る
        System.out.println(2 + 3 * 4); // 14
        System.out.println((2 + 3) * 4); // 20
    }
}
```

## 3.1.2
・Calculation.java（追記）
```
System.out.println(); // 改行

// 実数の計算
System.out.println(5.0 + 2); // 7.0
System.out.println(5.0 / 2); // 2.5
```

## 3.1.3
・Calculation.java（追記）
```
// 文字列の出力
System.out.println("test");
System.out.println("test" + "er"); // 文字の連結
System.out.println("test" + 123);  // 数値との連結
System.out.println("test" + (12 + 3)); // ()内が先に計算される。-> test15
```

## 3.1.4
・Calculation.java（追記）
```
System.out.println("文字列に\"を含む"); // 文字列に"を含む
```

## 3.1.5
・Calculation.java（追記）
```
System.out.println("""
        これは
        テキスト
        ブロック
        です
        """);
```

## 3.1.6
・Calculation.java（追記）
```
// これは1行コメント
/*
　これは複数行の
　コメント
 */
```

## 3.2.1
・Parameter.java
```
package basic.part3_2;

public class Parameter {
    public static void main(String[] args) {
        // 変数の宣言と代入
        int num = 24;
        System.out.println(num);

        String name = "田中";
        System.out.println(name);
    }
}
```

・Parameter.java（追記）
```
int num2;
num2 = 555; // すでに変数を宣言しているため、型の指定は不要。
```

## 3.2.3
・Parameter.java（追記）
```
// 変数同士の計算
int a = 5;
int b = 3;
System.out.println(a + b); // 8
int c = a * b;
System.out.println(c); // 15
int d = c - 5;
System.out.println(d); // 10

// 変数の再代入
int e = 5;
e = 14; 
System.out.println(e); // 14
```

## 3.2.4
・Parameter.java（追記）
```
// 複合代入演算子
int f = 20;
f += 2; // f = f + 2
System.out.println(f); // 22
f -= 2; // f = f - 2
System.out.println(f); // 20
f *= 2; // f = f * 2
System.out.println(f); // 40
f /= 2; // f = f / 2
System.out.println(f); // 20
```

## 3.2.5.2
・Parameter.java（追記）
```
// メソッドの利用
String str = "abcde";
System.out.println( str.toUpperCase() ); // ABCDE
```

## 3.2.6
・Parameter.java（追記）
```
// 整数->実数の型変換
int g = 10;
double h = g;
System.out.println(h); // 10.0

// 実数->整数の型変換
double i = 2.34;
int j = (int)i; // キャストという操作でデータの型を明示的に変換する。
System.out.println(j); // 小数点以下の情報が失われる -> 2

// 数値->文字列の型変換
int k = 30;
String l = String.valueOf(k);
System.out.println(l); // 30

// 文字列->数値の変換
String m = "1234";
int n = Integer.parseInt(m);
System.out.println(n); // 1234
```

## 3.2.7
・Parameter.java（追記）
```
// 定数
final double PI = 3.14;
System.out.println("円周率は" + PI);
```

## 3.2.8
・Parameter.java（追記）
```
// 推論型
var score = 87;
var subject = "数学";
System.out.println(subject + "の点数は" + score + "点です。");
```

## 3.2.9
・nullの使用例
```
String name = null;
System.out.println(name.toUpperCase()); // ここでエラーになる
```

## 3.3.1.1
・Condition.java
```
package basic.part3_3;

public class Condition {
    public static void main(String[] args) {
        // 値の大小比較
        System.out.println( 3 < 4 ); // true
        System.out.println( 8 < 2 ); // false
        System.out.println( 5 > 2 ); // true
        System.out.println( 5 > 5 ); // false

        // 等しいかどうか
        System.out.println( 2 == 2 ); // true
        System.out.println( 3 == 1 ); // false

        // 等しくないこと
        System.out.println( 5 != 2 ); // true
        System.out.println( 5 != 5 ); // false

        // 以下、もしくは以上
        System.out.println( 5 >= 5 ); // true
        System.out.println( 3 <= 9 ); // ture
    }
}
```

・Condition.java（追記）
```
// 文字列の比較
System.out.println( "apple".equals("banana") ); // false
System.out.println( "apple".equals("apple") ); // true
```

## 3.3.1.2
・Condition.java（追記）
```
// OR（論理和）はどちらか一方の条件がtrueの時にtrueとなる。
System.out.println( true || false ); // true
System.out.println( false || false ); // false
System.out.println( 5 > 2 || 3 == 2); // true

// AND（論理積）はどちらか両方の条件がtrueの時にtrueとなる。
System.out.println( true && false ); // false
System.out.println( true && true ); // true
System.out.println( 5 > 2 && 3 == 2 ); // false
```

## 3.3.1.3
・Condition.java（追記）
```
// 真偽値の反転
System.out.println( 5 > 2 ); // 5 は 2 より大きい -> true
System.out.println( !(5 > 2) ); // 5 は 2 より大きいを否定 -> false
```

## 3.3.2.1
・IfSample.java
```
package basic.part3_3;

public class IfSample {
    public static void main(String[] args) {
        // if文による処理分岐
        int a = 2;
        if (a < 5) {
            System.out.println(a + "は5より小さい");
        }
    }
}
```

・IfSample.java（追記）
```
// {} の省略
if (a == 2) System.out.println(a + "は2と等しい");
```

## 3.3.2.1.1
・IfSample.java（追記）
```
// else句
int b = 5;
if ( b < 3) {
    System.out.println(b + "は3より小さい");
}
else {
    System.out.println(b + "は3より大きい");
}
```

・IfSample.java（追記）
```
// else if句
int c = 20;
if ( c < 5 ) {
    System.out.println(c + "は5より小さい");
}
else if( c > 8 ) {
    System.out.println(c + "は8より大きい");
}
else {
    System.out.println(c + "は5より大きく、8より小さい");
}
```

## 3.3.2.2
・SwitchSample.java
```
package basic.part3_3;

public class SwitchSample {
    public static void main(String[] args) {
        // switch文による処理分岐
        int a = 3;
        switch (a) {
            case 1, 2 -> System.out.println("a is 1 or 2");
            case 3 -> System.out.println("a is 3");
            case 4 -> System.out.println("a is 4");
        }
    }
}
```

・SwitchSample.java（修正）
```
int a = 4;
switch (a) {
    case 1, 2 -> System.out.println("a is 1 or 2");
    case 3 -> System.out.println("a is 3");
    case 4 -> {
        System.out.print("a is "); // printの後ろのlnをとると改行せずに表示できる
        System.out.println("4");
    }
}
```

・SwitchSample.java（修正）
```
int a = 6;
switch (a) {
    case 1, 2 -> System.out.println("a is 1 or 2");
    case 3 -> System.out.println("a is 3");
    case 4 -> {
        System.out.print("a is "); // printの後ろのlnをとると改行せずに表示できます
        System.out.println("4");
    }
    default -> System.out.println("other");
}
```

## 3.3.2.3
・IfSample.java（追記）
```
// 三項演算子
int d = 3;
System.out.println( d < 5 ? "small" : "big" );
```

・IfSample.java（追記）
```
// テストの結果計算
int score = 68;
String result = score >= 60 ? "合格" : "不合格";
System.out.println( result );
```

## 3.4.1
・ForSample.java
```
package basic.part3_4;

public class ForSample {
    public static void main(String[] args) {
        // for文による繰り返し処理
        for (int i = 1; i <= 5; i++) {
            System.out.println( i + "回目のループ");
        }
    }
}
```

## 3.4.2
・ForSample.java（追記）
```
// ループをスキップ
for (int i = 1; i <= 5; i++) {
    if (i == 3) continue; // iが3のとき、ループをスキップ
    System.out.println( i + "回目のループ");
}
```

## 3.4.3
・ForSample.java（追記）
```
// ループの中断
for (int i = 1; i <= 5; i++) {
    if (i == 3) break; // iが3のとき、ループを中断
    System.out.println( i + "回目のループ");
}
```

## 3.4.4
・ForSample.java（追記）
```
// while文
int count = 5;
while(count < 30) {
    count += 2;
    System.out.println("count = " + count);
}
```

## 3.4.5
・ForSample.java（追記）
```
// do while文
int count2 = 5;
do {
    count2 += 2;
    System.out.println("count2 = " + count2);
}while (count2 < 30);
```

## 3.4.6
・ForSample.java（追記）
```
// 二重ループ
for (int i = 0; i < 5; i++) {
    for (int j = 0; j < 5; j++) {
        System.out.print(i + "行" + j + "列 ");
    }
    System.out.println(); // 改行
}
```

## 3.5.1
・Array.java
```
package basic.part3_5;

public class Array {
    public static void main(String[] args) {
        // 配列を扱う
        // 配列の宣言
        int[] numbers = new int[3];

        // 配列に値を代入
        numbers[0] = 1;
        numbers[1] = 5;
        numbers[2] = 32;

        // 配列の値を参照
        System.out.println( "0=" + numbers[0] );
        System.out.println( "1=" + numbers[1] );
        System.out.println( "2=" + numbers[2] );
    }
}
```

・Array.java（追記）
```
// 配列の宣言と値の設定
String[] names = new String[] {"tanaka", "ito", "saito"}; // 要素数を省略
int[] scores = { 20, 72, 88 }; // new 型[] を省略
```

・Array.java（追記）
```
// 配列の要素数
System.out.println( "names配列の要素数=" + names.length );
```

## 3.5.2
・Array.java（追記）
```
// 配列を使ったfor文
int[] ages = new int[]{ 24, 33, 54 };
for (int i = 0; i < ages.length; i++) {
    System.out.println(i + "番目の年齢は" + ages[i] + "歳");
}
```

## 3.5.3
・Array.java（追記）
```
// 多次元配列
int[][] matrix = {
        {1, 2, 3},
        {4, 5, 6}
};
System.out.println("1行目、2列目の要素=" + matrix[0][1]);
System.out.println("2行目、3列目の要素=" + matrix[1][2]);
```

## 3.5.4
・Array.java（追記）
```
// 拡張for
String[] fruits = {"りんご", "ばなな", "ぶどう"};
for(String fruit : fruits) {
    System.out.println(fruit);
}
```

## 3.6.1
・MethodSample.java
```
package basic.part3_6;

public class MethodSample {
    public static void main(String[] args) {
// メソッドの呼び出し
int sum_A = sum(5, 6);
        int sum_B = sum(3, 24);

        System.out.println("sum_A = " + sum_A);
        System.out.println("sum_B = " + sum_B);
    }

    // 足し算を行うメソッド
    static int sum(int a, int b) {
        int sum = a + b;
        return sum;
    }
}
```

## 3.6.2
・MethodSample.java（追記）
```
public class MethodSample {
    public static void main(String[] args) {


        〜中略〜

        // 名前を取得するメソッドの呼び出し
        String name = getName();
        System.out.println(name);
    }

    〜中略〜

    // 名前を取得するメソッド（引数の省略）
    static String getName() {
        return "tanaka";
    }
}
```

## 3.6.3
・MethodSample.java（追記）
```
public class MethodSample {
    public static void main(String[] args) {


        〜中略〜

        // 挨拶をするメソッドの呼び出し
        greeting();
    }

    〜中略〜

    // 挨拶をするメソッド（戻り値の省略）
    static void greeting() {
        System.out.println("こんにちは");
    }
}
```

・MethodSample.java（追記）
```
public class MethodSample {
    public static void main(String[] args) {


        〜中略〜

        // 点数判定メソッドの呼び出し
        checkScore(40);
        checkScore(88);
    }

    〜中略〜

    // 点数の判定メソッド（処理の中断）
    static void checkScore(int score) {
        if (score < 60) {
            System.out.println("不合格");
            return; // ここでメソッドの処理が終了される
        }
        System.out.println("合格");
    }
}
```

## 3.6.4
・MethodSample.java（追記）
```
public class MethodSample {
    public static void main(String[] args) {


        〜中略〜

        // 性別判定メソッドの呼び出し
        System.out.println(checkGender(1));
        System.out.println(checkGender(3));
    }

    〜中略〜

    // 性別判定メソッド（複数の戻り値）
    static String checkGender(int gender){
        if(gender == 1) {
            return "男";
        }
        else if(gender == 2) {
            return "女";
        }
        else {
            return "その他";
        }
    }
}
```

## 3.7.2
```
cd {コピーしたパス}

javac basic/part3_6/MethodSample.java

java -classpath {コピーしたパス} basic.part3_6.MethodSample
```

## 4.2.1

・Person.java
```
package basic.part4_2;

public class Person {
    // フィールド
    String name;
    int age;

    // メソッド
    void setInfo(String name, int age) {
        this.name = name;
        this.age = age;
    }
    void greeting() {
        System.out.println("私の名前は" + name + "です。年齢は" + age + "歳です。");
    }
}
```

・ClassSample.java
```
package basic.part4_2;

public class ClassSample {
    public static void main(String[] args) {
        // Personオブジェクトの生成
        Person person = new Person();

        // メソッドの呼び出し
        person.setInfo("田中", 24);
        person.greeting();

        // フィールドへのアクセス
        System.out.println(person.name);
    }
}
```

## 4.2.3
・Person.java（追記）
```
package basic.part4_2;

public class Person {
    // フィールド
    String name;
    int age;
    
    // コンストラクタ
    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // メソッド
    void setInfo(String name, int age) {
        this.name = name;
        this.age = age;
    }
    void greeting() {
        System.out.println("私の名前は" + name + "です。年齢は" + age + "歳です。");
    }
}
```

・ClassSample.java（修正）
```
package basic.part4_2;

public class ClassSample {
    public static void main(String[] args) {
        // Personオブジェクトの生成
        Person person = new Person("田中", 24);

        // メソッドの呼び出し
        person.greeting();

        // フィールドへのアクセス
        System.out.println(person.name);
    }
}
```

## 4.2.4
・Person.java（追記）
```
// staticフィールド
static String type = "哺乳類";

// staticメソッド
static void getType() {
    System.out.println("人は" + type + "です。");
}
```

・ClassSample.java（修正）
```
// staticフィールドへアクセス
System.out.println(Person.type);

// staticメソッドへアクセス
Person.getType();
```

## 4.3.1
・EncapsulationSample.java
```
package basic.part4_3;

import basic.part4_3.sub.Person;

public class EncapsulationSample {
    public static void main(String[] args) {
        Person p = new Person("佐藤", 42);
        p.greeting();
    }
}
```

・Person.java
```
package basic.part4_3.sub;

public class Person {
    String name;
    int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public void greeting() {
        System.out.println("私の名前は" + name + "です。年齢は" + age + "歳です。");
    }
}
```

4.3.4
・Car.java
```
package basic.part4_3.sub;

public class Car {
    private int speed;
    private String color;

    // デフォルトコンストラクタ（引数なし）
    public Car() {

    }

    // Getter
    public int getSpeed() {
        return speed;
    }
    public String getColor() {
        return color;
    }

    // Setter
    public void setSpeed(int speed) {
        this.speed = speed;
    }
    public void setColor(String color) {
        this.color = color;
    }
}
```

・EncapsulationSample.java（追記）
```
package basic.part4_3;

import basic.part4_3.sub.Person;
import basic.part4_3.sub.Car;

public class EncapsulationSample {
    public static void main(String[] args) {
        Person p = new Person("佐藤", 42);
        p.greeting();

        // JavaBeanを扱う
        Car c = new Car();
        c.setSpeed(120);
        c.setColor("黒");

        System.out.println("この車の速さは" +
                            c.getSpeed() + "km/h、色は" + c.getColor() + "です。");
    }
}
```

## 4.4
・Animal.java
```
package basic.part4_4;

public class Animal {
    private String type = "動物";

    public void showType() {
        System.out.println(type);
    }
}
```

・Dog.java
```
package basic.part4_4;

public class Dog extends Animal{
    private String name;

    public Dog(String name) {
        this.name = name;
    }

    public void showName() {
        System.out.println(name);
    }
}
```

・ExtendSample.java
```
package basic.part4_4;

public class ExtendSample {
    public static void main(String[] args) {
        Dog d = new Dog("ポチ");
        d.showName(); // 子クラスのメソッド
        d.showType(); // 親クラスのメソッド
    }
}
```

## 4.4.2
・Animal.java、Dog.java（追記）
```
public class Animal {
〜中略〜
    public void makeSound() {
        System.out.println("鳴き声");
    }
}

public class Dog extends Animal{
    〜中略〜
@Override
    public void makeSound() {
        System.out.println("ワンワン");
    }
}
```

## 4.4.3
・Animal.java、Dog.java（追記）
```
public class Animal {
    〜中略〜
    public Animal() {
        System.out.println("Animalのコンストラクタ");
    }
}

public class Dog extends Animal {
    〜中略〜
    public Dog(String name) {
        super();
        System.out.println("Dogのコンストラクタ");
        this.name = name;
    }
}
```

・Animal.java、Dog.java（追記）
```
public class Dog extends Animal{
    〜中略〜
    @Override
    public void makeSound() {
        super.makeSound();
        System.out.println("ワンワン");
    }
}
```

## 4.4.4
・Person.java
```
package basic.part4_4;

public abstract class Person {
    private String name;

    // 抽象メソッド。具象化は子クラスで行う
    public abstract void greeting();

    // 処理を持つメソッドも実装可能
    public void setName(String name) {
        this.name = name;
    }
    public String getName() {
        return this.name;
    }
}
```

・Student.java
```
package basic.part4_4;

public class Student extends Person {
    public Student(String name) {
        setName(name);
    }

    // 親クラスの抽象メソッドは子クラスで具象化する 
    @Override
    public void greeting() {
        System.out.println("私の名前は" + getName() + "です。学生です。");
    }
}
```

・ExtendSample.java（追記）
```
Student s = new Student("田中");
s.greeting();
```

## 4.4.5
・Teacher.java
```
package basic.part4_4;

public class Teacher extends Person {
    public Teacher(String name) {
        setName(name);
    }
    
    @Override
    public void greeting() {
        System.out.println("私の名前は" + getName() + "です。教師です。");
    }
}
```

・ExtendSample.java（追記）
```
// 親クラスの型の変数に、子クラスのインスタンスを代入
Person p1 = new Student("佐藤");
Person p2 = new Teacher("小島");

// 同じ型（Person）で、異なる振る舞いをする。（ポリモーフィズム）
p1.greeting();
p2.greeting();
```

## 4.5
・Animal.java
```
package basic.part4_5;

public interface Animal {
    void makeSound();
}
```

・Dog.java
```
package basic.part4_5;

public class Dog implements Animal{
    @Override
    public void makeSound() {
        System.out.println("ワンワン");
    }
}
```

・InterfaceSample.java
```
package basic.part4_5;

public class InterfaceSample {
    public static void main(String[] args) {
        Dog d = new Dog();
        d.makeSound();
    }
}
```

## 4.5.1
・Calculator.java
```
package basic.part4_5;

@FunctionalInterface
interface Calculator {
    int calculate(int a, int b);
}
```

・InterfaceSample.java（追記）
```
// 関数型インターフェース
Calculator add = (int a, int b) -> { return a + b; };
Calculator subtract = (int a, int b) -> { return a - b; };

System.out.println(add.calculate(10, 5)); // 15
System.out.println(subtract.calculate(10, 5)); // 5
```

## 4.6
・Box.java
```
package basic.part4_6;

public class Box<T> {
    private T value;

    public void set(T value) {
        this.value = value;
    }

    public T get() {
        return value;
    }
}
```

・GenericsSample.java
```
package basic.part4_6;

public class GenericsSample {
    public static void main(String[] args) {
        Box<String> stringBox = new Box<>();
        stringBox.set("hello");
        System.out.println(stringBox.get());

        Box<Integer> integerBox = new Box<>();
        integerBox.set(12345);
        System.out.println(integerBox.get());
    }
}
```

## 4.6.1
・Person.java
```
package basic.part4_6;

public class Person {
    <T> void showVal(T val) {
        System.out.println(val);
    }
}
```

・GenericsSample.java（追記）
```
Person p = new Person();
p.showVal(123);
p.showVal("test");
```

## 4.7.1
・Calculator.java
```
package basic.part4_7;

public class Calculator {
    public int division(int a, int b) {
        return a / b;
    }
}
```

・ExceptionSample.java
```
package basic.part4_7;

public class ExceptionSample {
    public static void main(String[] args) {
        Calculator c = new Calculator();
        int result = c.division(5, 0);

        System.out.println(result);
    }
}
```

・Calculator.java（修正）
```
package basic.part4_7;

public class Calculator {
    public int division(int a, int b) {
        int result = 0;
        try {
            result = a / b;
        }
        catch (ArithmeticException e) {
            System.out.println("システムエラー");
        }
        return result;
    }
}
```

## 4.7.4
・Calculator.java（修正）
```
package basic.part4_7;

public class Calculator {
    public int division(int a, int b) {
        if (b == 0) {
            throw new ArithmeticException();
        }
        int result = a / b;
        return result;
    }
}
```

・ExceptionSample.java（修正）
```
package basic.part4_7;

public class ExceptionSample {
    public static void main(String[] args) {
        Calculator c = new Calculator();
        int result = 0;
        try {
            result = c.division(5, 0);
        }
        catch (ArithmeticException e) {
            System.out.println("システムエラー");
        }
        System.out.println(result);
    }
}
```

## 5.2.1
・DateControl.java
```
package basic.part5_2;

import java.time.LocalDateTime;

public class DateControl {
    public static void main(String[] args) {
        LocalDateTime now = LocalDateTime.now();
        System.out.println(now);
    }
}
```

## 5.2.2
・DateControl.java（追記）
```
LocalDateTime birthday = LocalDateTime.of(2000, 1, 1, 12, 0);
System.out.println(birthday);
```

## 5.2.3
・DateControl.java（追記）
```
LocalDateTime future = LocalDateTime.now().plusDays(5); // 5日後
System.out.println(future);

LocalDateTime past = LocalDateTime.now().minusMonths(2); // 2か月前
System.out.println(past);
```

## 5.2.4
・DateControl.java（追記）
```
DateTimeFormatter formatter = DateTimeFormatter.ofPattern("yyyy/MM/dd HH:mm");
String formatted = now.format(formatter);
System.out.println(formatted);
```

## 5.3.1
・CollectionSample.java
```
package basic.part5_3;

import java.util.ArrayList;

public class CollectionSample {
    public static void main(String[] args) {
        // Listを使う
        ArrayList<String> fruits = new ArrayList<>();

        fruits.add("りんご");
        fruits.add("バナナ");
        fruits.add("みかん");

        System.out.println(fruits); // [りんご, バナナ, みかん]
        System.out.println(fruits.get(0)); // りんご
        System.out.println(fruits.size()); // 3
    }
}
```

## 5.3.2
・CollectionSample.java（追記）
```
// Setを使う
HashSet<String> colors = new HashSet<>();

colors.add("赤");
colors.add("青");
colors.add("緑");
colors.add("赤"); // 重複なので無視される

System.out.println(colors); // 順番はバラバラ、重複なし
```

## 5.3.3
・CollectionSample.java（追記）
```
// Mapを使う
HashMap<String, Integer> scores = new HashMap<>();

scores.put("たろう", 90);
scores.put("はなこ", 80);
scores.put("じろう", 70);

System.out.println(scores); // {たろう=90, はなこ=80, じろう=70}
System.out.println(scores.get("たろう")); // 90
```

## 5.3.4
・CollectionSample.java（追記）
```
// コレクションの処理
ArrayList<String> students = new ArrayList<>();

students.add("たろう");
students.add("はなこ");
students.add("じろう");

for (int i = 0; i < students.size(); i++) {
    System.out.println("forで出力: " + students.get(i));
}

for (String student : students) {
    System.out.println("拡張forで出力: " + student);
}
```

## 5.4.1
・SwingSample.java
```
package basic.part5_4;

import javax.swing.*;

public class SwingSample {
    public static void main(String[] args) {
        // ウィンドウの作成
        JFrame frame = new JFrame("はじめてのSwing");

        frame.setSize(400, 300); // サイズ設定
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE); // 閉じるボタンで終了
        frame.setVisible(true); // ウィンドウを表示
    }
}
```

## 5.4.2
・SwingSample.java（追記）
```
public static void main(String[] args) {
    // ウィンドウの作成
    JFrame frame = new JFrame("はじめてのSwing");

    frame.setSize(400, 300); // サイズ設定
    frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE); // 閉じるボタンで終了
    frame.setLayout(null); // レイアウトを自由配置にする

    JButton button = new JButton("押してね！");
    button.setBounds(50, 100, 120, 30); // (x, y, width, height)

    JLabel label = new JLabel("こんにちは！");
    label.setBounds(50, 50, 200, 30);

    frame.add(button);
    frame.add(label);

    frame.setVisible(true); // ウィンドウを表示
}
```

## 5.4.3
・SwingSample.java（追記）
```
// ボタンにイベントを設定する
button.addActionListener(e -> label.setText("ボタンが押された！"));
```

## 5.5.1
・StreamSample.java
```
package basic.part5_5;

import java.util.ArrayList;
import java.util.List;

public class StreamSample {
    public static void main(String[] args) {
        ArrayList<String> fruits = new ArrayList<>(List.of("りんご", "バナナ", "みかん"));

        fruits.stream()  // ストリームを作る
                .forEach(fruit -> System.out.println(fruit)); // 1個ずつ表示
    }
}
```

## 5.5.2
・StreamSample.java（修正）
```
fruits.stream()  // ストリームを作る
        .filter(name -> name.endsWith("ナナ")) // 「ナナ」で終わる果物だけを抽出
        .forEach(fruit -> System.out.println(fruit)); // 1個ずつ表示
```

## 5.5.3
・StreamSample.java（修正）
```
fruits.stream()  // ストリームを作る
        .map(fruit -> fruit.toUpperCase()) // 大文字に変換
        .forEach(fruit -> System.out.println(fruit)); // 1個ずつ表示
```

## 5.5.4
・StreamSample.java（修正）
```
fruits.stream()  // ストリームを作る
        .sorted() // 昇順で並び替え
        .forEach(fruit -> System.out.println(fruit)); // 1個ずつ表示
```

## 5.6.4
・HttpClientSample.java
```
package basic.part5_6;

import java.net.URI;
import java.net.http.HttpClient;
import java.net.http.HttpRequest;
import java.net.http.HttpResponse;

public class HttpClientSample {
    public static void main(String[] args) {
        try {
            // HTTP通信を行うクライアントオブジェクトを生成
            HttpClient client = HttpClient.newHttpClient();

            // 要求（リクエスト）の内容を定義
            HttpRequest request = HttpRequest.newBuilder()
                    .uri(new URI("http://example.com"))
                    .GET()
                    .build();

            // 通信を行い、サーバーからの回答（レスポンス）を受領
            HttpResponse<String> response = client.send(request, HttpResponse.BodyHandlers.ofString());

            // レスポンスの内容をコンソールへ表示
            System.out.println("ステータスコード: " + response.statusCode());
            System.out.println("レスポンス内容: ");
            System.out.println(response.body());

        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

## 5.6.10
・HttpServerSample.java
```
package basic.part5_6;

import com.sun.net.httpserver.HttpServer;

import java.io.IOException;
import java.io.OutputStream;
import java.net.InetSocketAddress;

public class HttpServerSample {
    public static void main(String[] args) throws IOException {
        // ポート8000でサーバーを作成
        HttpServer server = HttpServer.create(new InetSocketAddress(8000), 0);

        // "/hello"パスにリクエストが来たときに呼ばれるイベントを設定
        server.createContext("/hello", e -> {
            String response = "Hello, World!";
            e.sendResponseHeaders(200, response.length()); // ステータス200を返す
            OutputStream os = e.getResponseBody();
            os.write(response.getBytes());
            os.close();
        });
        
        // サーバーをスタート
        server.start();
        System.out.println("Server started at http://localhost:8000/");
    }
}
```

## 6.2.2
・pom.xml
```
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <!-- プロジェクト基本情報 -->
    <groupId>org.example</groupId>
    <artifactId>javaProject</artifactId>
    <version>1.0-SNAPSHOT</version>

    <!-- Javaのバージョンや文字コード -->
    <properties>
        <maven.compiler.source>24</maven.compiler.source>
        <maven.compiler.target>24</maven.compiler.target>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    </properties>

</project>
```

## 6.2.3
・pom.xml（追記）
```
<!-- 依存関係（ライブラリ） -->
<dependencies>
    <dependency>
       <groupId>org.apache.commons</groupId>
       <artifactId>commons-lang3</artifactId>
       <version>3.12.0</version>
       <scope>compile</scope>
    </dependency>
</dependencies>
```

・MavenSample.java
```
package basic.part6_2;

import org.apache.commons.lang3.StringUtils;

public class MavenSample {
    public static void main(String[] args) {
        String str = "";
        if (StringUtils.isBlank(str)) {
            System.out.println("文字列は空または空白だけです");
        } else {
            System.out.println("文字列に何か入っています");
        }
    }
}
```

## 6.2.4
・pom.xml（追記）
```
<!-- ビルド設定 -->
<build>
    <plugins>
        <!-- 実行可能JARにするプラグイン（エントリーポイントの設定） -->
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-jar-plugin</artifactId>
            <version>3.3.0</version>
            <configuration>
                <archive>
                    <manifest>
                        <mainClass>basic.part6_2.MavenSample</mainClass>
                    </manifest>
                </archive>
            </configuration>
        </plugin>

        <!-- 依存ライブラリをJARに含めるプラグイン -->
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-shade-plugin</artifactId>
            <version>3.5.0</version>
            <executions>
                <execution>
                    <phase>package</phase>
                    <goals>
                        <goal>shade</goal>
                    </goals>
                </execution>
            </executions>
        </plugin>
    </plugins>
</build>
```

## 6.3.1
・JavadocSample.java
```
package basic.part6_3;

public class JavadocSample {
    public static void main(String[] args) {
        Person p = new Person();
        String introduction = p.createIntroduction("田中");
        System.out.println(introduction);
    }
}
```

・Person.java
```
package basic.part6_3;

/**
 * 人を表すクラス
 */
public class Person {
    /**
     * 自己紹介文を作成する。
     *
     * @param name 自己紹介をする本人の名前
     * @return 自己紹介文
     */
    public String createIntroduction(String name) {
        return "私の名前は" + name + "です。";
    }
}
```

## 6.4.1
・pom.xml（追記）
```
<!-- JUnit -->
<dependency>
    <groupId>org.junit.jupiter</groupId>
    <artifactId>junit-jupiter</artifactId>
    <version>5.10.5</version>
    <scope>test</scope>
</dependency>
```

## 6.4.2
・ScoreCalculator.java
```
package basic.part6_4;

public class ScoreCalculator {
    private int score;

    public ScoreCalculator() {
        score = 0;
    }

    // スコアの加算処理
    public int addScore(int add) {
        score += add;

        // scoreが100より大きくならないようにする。
        if(score > 90) {
            score = 100;
        }

        return score;
    }
}
```

・ScoreCalculatorTest.java
```
package basic.part6_4;

import org.junit.jupiter.api.Test;

import static org.junit.jupiter.api.Assertions.*;
class ScoreCalculatorTest {

    @Test
    void addScore() {
    }
}
```

## 6.4.3
・ScoreCalculatorTest.java（追記）
```
package basic.part6_4;

import org.junit.jupiter.api.Test;

import static org.junit.jupiter.api.Assertions.*;
class ScoreCalculatorTest {

    @Test
    void addScore() {
        // テストの準備
        // テスト対象クラスをインスタンス化する
        ScoreCalculator sc = new ScoreCalculator();

        // scoreに10を加算し、結果が10であること
        int score = sc.addScore(10); // テスト条件
        assertEquals(10, score); // 期待値の確認
    }
}
```

## 6.4.4
・ScoreCalculatorTest.java（追記）
```
@Test
void addScore() {
    // テストの準備
    // テスト対象クラスをインスタンス化する
    ScoreCalculator sc = new ScoreCalculator();

    // scoreに10を加算し、結果が10であること
    int score = sc.addScore(10); // テスト条件
    assertEquals(10, score); // 期待値の確認

    // scoreに30を加算し、結果が40であること
    score = sc.addScore(30);
    assertEquals(40, score);

    // scoreに59を加算し、結果が99であること ※境界値分析
    score = sc.addScore(59);
    assertEquals(99, score);

    // scoreに1を加算し、結果が100であること ※境界値分析
    score = sc.addScore(1);
    assertEquals(100, score);

    // scoreに50を加算し、結果が100であること
    score = sc.addScore(50);
    assertEquals(100, score);
}
```

・ScoreCalculator.java（修正）
```
// scoreが100より大きくならないようにする。
if(score > 100) {
    score = 100;
}
```

## 6.5.1.1
## 6.5.1.2
・インストール確認のコマンド
```
git --version
```

## 6.5.2
・Git初期設定
```
git config --global user.name "ユーザー名"
git config --global user.email "メールアドレス"
```

・設定内容確認
```
git config user.name
git config user.email
```

## 6.5.3.1
・ローカルリポジトリの作成
```
cd {javaProject のパス}
git init
```

## 6.5.3.2
・ステージングに登録
```
git add src/main/java/HelloWorld.java
```

## 6.5.3.3
・ステータスの確認
```
git status
```

## 6.5.3.4
・コミットの実行
```
git commit -m "最初のコミット"
```

## 6.5.3.5
・コミットログの確認
```
git log
```

## 6.5.3.6
・HelloWorld.java（追記）
```
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World!");
        System.out.println("追記");
    }
}
```

・HelloWorld.javaのコミット
```
git add src/main/java/HelloWorld.java
git commit -m "2回目のコミット"
```

・コミットの反映確認
```
git log
```

・前のコミットに戻す
```
git reset {戻す先のコミット番号}
```

## 6.5.4.1
・ブランチの作成
```
git branch sampleBranch
```

## 6.5.4.2
・ブランチの一覧表示
```
git branch
```

・ブランチの切り替え
```
git checkout sampleBranch
```

## 6.5.4.3
・HelloWorld.java（追記）
```
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World!");
        System.out.println("サンプルブランチ用コード");
    }
}
```

・HelloWorld.javaのコミット
```
git add src/main/java/HelloWorld.java
git commit -m "サンプルブランチのコミット"
```

・mainブランチへの切り替え
```
git checkout main
```

・sampleBranchのマージ
```
git merge sampleBranch
```

## 6.5.4.4
・ブランチの削除
```
git branch -d sampleBranch
```

## 6.5.5.2
・リモートリポジトリの追加
```
git remote add {リモート名} {リモートURL}
```

## 6.5.5.4
・リモートへの反映
```
git push -u {リモート名} {追加したいブランチ名}
```

## 6.5.5.5
・リモートからの取得
```
git pull
```

## 6.5.5.6
・リポジトリの複製
```
git clone {複製元のリモートリポジトリURL}
```

## 7.3.2
・HelloController.java
```
package com.webAppDev.tasklist.controller;

import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class HelloController {
    @GetMapping("/hello")
    public String hello() {
        return "Hello, World!";
    }
}
```

## 7.3.3.1
・TaskListController.java
```
package com.webAppDev.tasklist.controller;

import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestMapping;

@Controller
@RequestMapping("tasklist")
public class TaskListController {

    @GetMapping
    public String showlist(Model model) {
        model.addAttribute("msg", "タスク管理アプリケーション");
        return "tasklist";
    }
}
```

・tasklist.html
```
<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org">
<head>
    <meta charset="UTF-8">
    <title>タスク管理アプリケーション</title>
</head>
<body>
    <h1 th:text="${msg}"></h1>
</body>
</html>
```

## 7.3.3.2
・Task.java
```
package com.webAppDev.tasklist.entity;

import java.time.LocalDateTime;

public class Task {
    private int id;
    private String title;
    private String detail;
    private LocalDateTime deadline;
    private boolean state; // false:未完了 true:完了

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getTitle() {
        return title;
    }

    public void setTitle(String title) {
        this.title = title;
    }

    public String getDetail() {
        return detail;
    }

    public void setDetail(String detail) {
        this.detail = detail;
    }

    public LocalDateTime getDeadline() {
        return deadline;
    }

    public void setDeadline(LocalDateTime deadline) {
        this.deadline = deadline;
    }

    public boolean isState() {
        return state;
    }

    public void setState(boolean state) {
        this.state = state;
    }
}
```

・TaskRepository.java
```
package com.webAppDev.tasklist.repository;

import com.webAppDev.tasklist.entity.Task;

import java.util.List;

public interface TaskRepository {
    List<Task> findAll(); // 全タスクの取得
    void save(Task task); // タスクの登録
}
```

・TaskRepositoryImpl.java
```
package com.webAppDev.tasklist.repository;

import com.webAppDev.tasklist.entity.Task;
import org.springframework.stereotype.Repository;

import java.util.ArrayList;
import java.util.List;

@Repository
public class TaskRepositoryImpl implements TaskRepository {
    // タスクの情報を保持するリスト
    private List<Task> tasklist = new ArrayList<>();

    @Override
    public List<Task> findAll() {
        return tasklist;
    }

    @Override
    public void save(Task task) {
        tasklist.add(task);
    }
}
```

・TaskListService.java
```
package com.webAppDev.tasklist.service;

import com.webAppDev.tasklist.entity.Task;

import java.util.List;

public interface TaskListService {
    List<Task> getTaskList();
    String addTask(String title, String detail, String deadline);
}
```

・TaskListServiceImpl.java
```
package com.webAppDev.tasklist.service;

import com.webAppDev.tasklist.entity.Task;
import com.webAppDev.tasklist.repository.TaskRepository;
import org.springframework.stereotype.Service;

import java.time.LocalDateTime;
import java.util.List;

@Service
public class TaskListServiceImpl implements TaskListService {

    private final TaskRepository taskRepository;

    /**
     * コンストラクタ。DIによりtaskRepositoryを初期化。
     * @param taskRepository
     */
    public TaskListServiceImpl(TaskRepository taskRepository) {
        this.taskRepository = taskRepository;
    }

    /**
     * タスクを全件取得
     * @return タスクの一覧
     */
    @Override
    public List<Task> getTaskList() {
        return taskRepository.findAll();
    }

    /**
     * タスクの登録処理
     * @param title
     * @param detail
     * @param deadline
     * @return 処理結果のテキスト。成功時は空文字を返す。
     */
    @Override
    public String addTask(String title, String detail, String deadline) {
        // バリデーションチェック
        // タスク名は10文字より大きい、もしくは0文字の場合エラー。
        if(title.length() > 10 || title.isEmpty())
            return "タスク名は1文字以上10文字以下です";
        // タスク詳細は100文字より大きい場合エラー。
        if(detail.length() > 100)
            return "タスク詳細は100文字以下です";

        // 現在の総タスク数+1をIDとする。
        int taskId = taskRepository.findAll().size() + 1;

        // deadlineはStringで受け取っているため、LocalDateTimeへ変換する。
        // なお引数が空文字の場合は、LocalDateTime.parse()でエラーとなるためnullを設定する。
        LocalDateTime _deadline = deadline.isEmpty() ? null : LocalDateTime.parse(deadline);

        // Taskオブジェクトへの詰め替え処理
        Task task = new Task();
        task.setId(taskId);
        task.setTitle(title);
        task.setDetail(detail);
        task.setDeadline(_deadline);
        task.setState(false); // タスク未完了状態をセット。

        // タスクの登録処理
        taskRepository.save(task);
        return "";
    }
}
```

## 7.3.3.4
・TaskListController.java（修正）
```
@Controller
@RequestMapping("tasklist")
public class TaskListController {

    // サービスクラスのインスタンス
    private final TaskListService taskListService;

    /**
     * コンストラクタ。DIによりtaskListServiceを初期化。
     * @param taskListService
     */
    public TaskListController(TaskListService taskListService) {
        this.taskListService = taskListService;
    }

    /**
     * タスク一覧の表示
     * @param model
     * @return resources/templates下のHTMLファイル名
     */
    @GetMapping
    public String showlist(Model model) {
        List<Task> list = taskListService.getTaskList();
        model.addAttribute("list", list);
        return "tasklist";
    }

    /**
     * タスクの追加
     * @return resources/templates下のHTMLファイル名
     */
    @PostMapping("addtask")
    public String addTask(@RequestParam String title,
                          @RequestParam String detail,
                          @RequestParam String deadline,
                          Model model) {
        // タスクの登録
        String result = taskListService.addTask(title, detail, deadline);

        // 戻り値が""ではない時、エラーと判定。
        // エラーメッセージと入力途中の情報をmodelに設定。
        if (!result.isEmpty()) {
            model.addAttribute("errorMsg", result);
            model.addAttribute("title", title);
            model.addAttribute("detail", detail);
            model.addAttribute("deadline", deadline);
        }

        // タスク一覧をmodelに設定。
        List<Task> list = taskListService.getTaskList();
        model.addAttribute("list", list);
        return "tasklist";
    }
}
```

・tasklist.html（修正）
```
<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org">
<head>
    <meta charset="UTF-8">
    <title>タスク管理アプリケーション</title>
</head>
<body>
    <!-- タスク登録フォーム -->
    <h3>タスク登録</h3>
    <form th:action="@{/tasklist/addtask}" method="post">
        <div>
            <label for="title">タスク名: </label>
            <input type="text" id="title" name="title" th:value="${title}"/>
        </div>
        <div>
            <label for="detail">タスク詳細: </label>
            <input type="text" id="detail" name="detail" th:value="${detail}">
        </div>
        <div>
            <label for="deadline">期日: </label>
            <input type="datetime-local" id="deadline" name="deadline" th:value="${deadline}"/>
        </div>
        <div>
            <button type="submit">追加</button>
            <p th:if="${errorMsg}" th:text="${errorMsg}" style="color: red;"></p>
        </div>
    </form>

    <!-- タスク一覧の表示 -->
    <h3>タスク一覧</h3>
    <table>
        <thead>
            <tr>
                <th>ID</th>
                <th>タスク名</th>
                <th>タスク詳細</th>
                <th>期日</th>
                <th>ステータス</th>
            </tr>
        </thead>
        <tbody>
            <tr th:each="obj : ${list}">
                <td th:text="${obj.id}"></td>
                <td th:text="${obj.title}"></td>
                <td th:text="${obj.detail}"></td>
                <td th:text="${obj.deadline}"></td>
                <td th:text="${obj.state} ? '完了' : '未完了'"></td>
            </tr>
        </tbody>
    </table>

</body>
</html>
```

・TaskRepository.java（修正）
```
public interface TaskRepository {
    List<Task> findAll(); // 全タスクの取得
    void save(Task task); // タスクの登録
    void update(Task task); // タスクの更新
    void deleteById(int id); // タスクの削除
    Task findById(int id); // タスクの検索
}
```

・TaskRepositoryImpl.java（修正）
```
@Repository
public class TaskRepositoryImpl implements TaskRepository {
    〜 省略 〜

    @Override
    public void update(Task task) {
        deleteById(task.getId());
        tasklist.add(task);
    }

    @Override
    public void deleteById(int id) {
        for(Task t : tasklist) {
            if(t.getId() == id) {
                tasklist.remove(t);
                return;
            }
        }
    }

    @Override
    public Task findById(int id) {
        for(Task t : tasklist) {
            if(t.getId() == id) {
                return t;
            }
        }
        return null;
    }
}
```

・TaskListService.java（修正）
```
public interface TaskListService {
    List<Task> getTaskList();
    String addTask(String title, String detail, String deadline);
    void updateTask(Task task);
    void deleteTask(int id);
    Task findTask(int id);
}
```

・TaskListServiceImpl.java（修正）
```
@Service
public class TaskListServiceImpl implements TaskListService {


    〜 省略 〜

    /**
     * タスクの更新
     * @param task
     * @return
     */
    @Override
    public void updateTask(Task task) {
        taskRepository.update(task);
    }

    /**
     * タスクの削除
     * @param id
     */
    @Override
    public void deleteTask(int id) {
        taskRepository.deleteById(id);
    }

    /**
     * idをキーとし、タスクを検索
     * @param id
     * @return 検索結果のタスク
     */
    @Override
    public Task findTask(int id) {
        return taskRepository.findById(id);
    }
}
```

## 7.3.4.3
・pom.xml（追記）
```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-validation</artifactId>
</dependency>
```

・TaskForm.java
```
package com.webAppDev.tasklist.dto;

import jakarta.validation.constraints.Future;
import jakarta.validation.constraints.NotNull;
import jakarta.validation.constraints.Size;
import org.springframework.format.annotation.DateTimeFormat;

import java.time.LocalDateTime;

public class TaskForm {
    private int id;

    @NotNull (message = "必須入力です。")
    @Size(min = 1, max = 10, message = "10文字以内で入力してください。")
    private String title;

    @Size(max = 100, message = "100文字以内で入力してください。")
    private String detail;

    @DateTimeFormat(pattern = "yyyy-MM-dd'T'HH:mm")
    @Future(message = "期限が過去に設定されています。")
    private LocalDateTime deadline;

    private boolean state; // false:未完了 true:完了

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }
    public String getTitle() {
        return title;
    }

    public void setTitle(String title) {
        this.title = title;
    }

    public String getDetail() {
        return detail;
    }

    public void setDetail(String detail) {
        this.detail = detail;
    }

    public LocalDateTime getDeadline() {
        return deadline;
    }

    public void setDeadline(LocalDateTime deadline) {
        this.deadline = deadline;
    }

    public boolean isState() {
        return state;
    }

    public void setState(boolean state) {
        this.state = state;
    }

}
```

## 7.3.4.4
・tasklist.html（修正）
```
<!-- タスク一覧の表示 -->
<h3>タスク一覧</h3>
<table>
    <thead>
        <tr>
            <th>ID</th>
            <th>タスク名</th>
            <th>タスク詳細</th>
            <th>期日</th>
            <th>ステータス</th>
            <th>編集</th>
            <th>削除</th>
        </tr>
    </thead>
    <tbody>
        <tr th:each="obj : ${list}">
            <td th:text="${obj.id}"></td>
            <td th:text="${obj.title}"></td>
            <td th:text="${obj.detail}"></td>
            <td th:text="${obj.deadline}"></td>
            <td th:text="${obj.state} ? '完了' : '未完了'"></td>
            <td>
                <a type="button" th:href="@{/tasklist/edittask(id=${obj.id})}">編集</a>
            </td>
            <td>
                <form th:action="@{/tasklist/deletetask}" method="POST">
                    <input type="hidden" name="id" th:value="${obj.id}">
                    <button type="submit">削除</button>
                </form>
            </td>
        </tr>
    </tbody>
</table>
```

・edittask.html
```
<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org">
<head>
    <meta charset="UTF-8">
    <title>タスク管理アプリケーション</title>
</head>
<body>
<!-- タスク編集フォーム -->
<h3>タスク編集</h3>
<form th:action="@{/tasklist/updatetask}" method="post" th:object="${taskForm}">
    <input type="hidden" name="id" th:field="*{id}">
    <div>
        <label for="title">タスク名: </label>
        <input type="text" id="title" name="title" th:field="*{title}"/>
        <p th:if="${#fields.hasErrors('title')}" th:errors="*{title}" style="color: red;"></p>
    </div>
    <div>
        <label for="detail">タスク詳細: </label>
        <input type="text" id="detail" name="detail" th:field="*{detail}">
        <p th:if="${#fields.hasErrors('detail')}" th:errors="*{detail}" style="color: red;"></p>
    </div>
    <div>
        <label for="deadline">期日: </label>
        <input type="datetime-local" id="deadline" name="deadline" th:field="*{deadline}"/>
        <p th:if="${#fields.hasErrors('deadline')}" th:errors="*{deadline}" style="color: red;"></p>
    </div>
    <div>
        <label for="state">ステータス: </label>
        <select id="state" name="state" th:field="*{state}">
            <option th:value="true">完了</option>
            <option th:value="false">未完了</option>
        </select>
    </div>
    <div>
        <button type="submit">確定</button>
    </div>
</form>
</body>
</html>
```

・TaskListController.java（修正）
```
@Controller
@RequestMapping("tasklist")
public class TaskListController {


    〜 省略 〜

    /**
     * タスク編集画面への移動
     * @param id
     * @param model
     * @return resources/templates下のHTMLファイル名
     */
    @GetMapping("edittask")
    public String editTask(@RequestParam int id,
                           Model model) {
        Task task = taskListService.findTask(id);

        // formオブジェクトへ詰め替え
        TaskForm taskForm = new TaskForm();
        taskForm.setId(task.getId());
        taskForm.setTitle(task.getTitle());
        taskForm.setDetail(task.getDetail());
        taskForm.setDeadline(task.getDeadline());
        taskForm.setState(task.isState());

        // Thymeleafへformオブジェクトを渡す
        model.addAttribute("taskForm", taskForm);
        return "edittask";
    }

    /**
     * タスクの更新
     * @param taskForm
     * @param result
     * @param model
     * @return resources/templates下のHTMLファイル名
     */
    @PostMapping("updatetask")
    public String updateTask(@ModelAttribute @Valid TaskForm taskForm,
                             BindingResult result,
                             Model model) {
        // バリデーションチェック結果判定
        if(!result.hasErrors()){
            // エラーがない場合の処理
            // Taskオブジェクトへ詰め替え
            Task task = new Task();
            task.setId(taskForm.getId());
            task.setTitle(taskForm.getTitle());
            task.setDetail(taskForm.getDetail());
            task.setDeadline(taskForm.getDeadline());
            task.setState(taskForm.isState());

            // Serviceクラスの更新処理を呼び出す
            taskListService.updateTask(task);
            return "redirect:/tasklist";
        }
        else {
            // エラーの場合、再度フォームオブジェクトをフロントへ渡し
            // タスク編集画面を表示
            model.addAttribute("taskForm", taskForm);
            return "edittask";
        }
    }

    /**
     * タスクの削除
     * @param id
     * @param model
     * @return resources/templates下のHTMLファイル名
     */
    @PostMapping("deletetask")
    public String deleteTask(@RequestParam int id,
                             Model model) {
        taskListService.deleteTask(id);
        return "redirect:/tasklist";
    }
}
```

## 7.3.4.5
・tasklist.html（修正）
```
<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org">
<head>
    <meta charset="UTF-8">
    <title>タスク管理アプリケーション</title>
    <!-- Bootstrap CSSの読み込み -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body class="bg-light py-5">

<div class="container">
    <!-- タスク登録フォーム -->
    <h3 class="mb-4">タスク登録</h3>
    <form th:action="@{/tasklist/addtask}" method="post" class="bg-white p-4 rounded shadow-sm mb-5">
        <div class="mb-3">
            <label for="title" class="form-label">タスク名</label>
            <input type="text" id="title" name="title" th:value="${title}" class="form-control"/>
        </div>
        <div class="mb-3">
            <label for="detail" class="form-label">タスク詳細</label>
            <input type="text" id="detail" name="detail" th:value="${detail}" class="form-control"/>
        </div>
        <div class="mb-3">
            <label for="deadline" class="form-label">期日</label>
            <input type="datetime-local" id="deadline" name="deadline" th:value="${deadline}" class="form-control"/>
        </div>
        <div class="text-end">
            <button type="submit" class="btn btn-success">追加</button>
        </div>
        <div th:if="${errorMsg}" class="text-danger mt-2" th:text="${errorMsg}"></div>
    </form>

    <!-- タスク一覧の表示 -->
    <h3 class="mb-3">タスク一覧</h3>
    <div class="table-responsive">
        <table class="table table-striped table-bordered align-middle bg-white shadow-sm">
            <thead class="table-light">
            <tr>
                <th>ID</th>
                <th>タスク名</th>
                <th>タスク詳細</th>
                <th>期日</th>
                <th>ステータス</th>
                <th>編集</th>
                <th>削除</th>
            </tr>
            </thead>
            <tbody>
            <tr th:each="obj : ${list}">
                <td th:text="${obj.id}"></td>
                <td th:text="${obj.title}"></td>
                <td th:text="${obj.detail}"></td>
                <td th:text="${obj.deadline}"></td>
                <td th:text="${obj.state} ? '完了' : '未完了'"></td>
                <td>
                    <a th:href="@{/tasklist/edittask(id=${obj.id})}" class="btn btn-primary btn-sm">編集</a>
                </td>
                <td>
                    <form th:action="@{/tasklist/deletetask}" method="POST">
                        <input type="hidden" name="id" th:value="${obj.id}">
                        <button type="submit" class="btn btn-danger btn-sm">削除</button>
                    </form>
                </td>
            </tr>
            </tbody>
        </table>
    </div>
</div>

</body>
</html>
```

・edittask.html（修正）
```
<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org">
<head>
    <meta charset="UTF-8">
    <title>タスク管理アプリケーション</title>
    <!-- Bootstrap CSSの読み込み -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body class="bg-light py-5">

<div class="container">
    <h3 class="mb-4">タスク編集</h3>
    <form th:action="@{/tasklist/updatetask}" method="post" th:object="${taskForm}" class="bg-white p-4 rounded shadow-sm">
        <input type="hidden" name="id" th:field="*{id}">

        <div class="mb-3">
            <label for="title" class="form-label">タスク名</label>
            <input type="text" id="title" name="title" th:field="*{title}" class="form-control"/>
            <div th:if="${#fields.hasErrors('title')}" th:errors="*{title}" class="text-danger small"></div>
        </div>

        <div class="mb-3">
            <label for="detail" class="form-label">タスク詳細</label>
            <input type="text" id="detail" name="detail" th:field="*{detail}" class="form-control"/>
            <div th:if="${#fields.hasErrors('detail')}" th:errors="*{detail}" class="text-danger small"></div>
        </div>

        <div class="mb-3">
            <label for="deadline" class="form-label">期日</label>
            <input type="datetime-local" id="deadline" name="deadline" th:field="*{deadline}" class="form-control"/>
            <div th:if="${#fields.hasErrors('deadline')}" th:errors="*{deadline}" class="text-danger small"></div>
        </div>

        <div class="mb-3">
            <label for="state" class="form-label">ステータス</label>
            <select id="state" name="state" th:field="*{state}" class="form-select">
                <option th:value="true">完了</option>
                <option th:value="false">未完了</option>
            </select>
        </div>

        <div class="text-end">
            <button type="submit" class="btn btn-primary">確定</button>
        </div>
    </form>
</div>

</body>
</html>
```

## 7.3.5
・pom.xml（追記）
```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-aop</artifactId>
</dependency>
```

・LoggingAspect.java
```
package com.webAppDev.tasklist.aspect;

import org.aspectj.lang.JoinPoint;
import org.aspectj.lang.annotation.After;
import org.aspectj.lang.annotation.Aspect;
import org.aspectj.lang.annotation.Before;
import org.aspectj.lang.annotation.Pointcut;
import org.springframework.stereotype.Component;

@Aspect
@Component
public class LoggingAspect {
    @Pointcut("execution(* com.webAppDev.tasklist.controller.TaskListController.*(..))")
    public void controllerMethods() {}

    @Before("controllerMethods()")
    public void beforeMethod(JoinPoint joinPoint) {
        System.out.println("コントローラーメソッドの開始: " + joinPoint.getSignature());
    }

    @After("controllerMethods()")
    public void afterMethod(JoinPoint joinPoint) {
        System.out.println("コントローラーメソッドの終了: " + joinPoint.getSignature());
    }

}
```

## 7.4.3
・pom.xml（追記）
```
<dependency>
    <groupId>com.h2database</groupId>
    <artifactId>h2</artifactId>
    <scope>runtime</scope>
</dependency>
```

・application.properties（追記）
```
# Enable H2 console
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

# Data source setup
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.url=jdbc:h2:./h2db/taskdb
spring.datasource.username=sa
spring.datasource.password=12345
```

## 7.4.4.1
```
CREATE TABLE task (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(10) NOT NULL,
    detail VARCHAR(100),
    deadline TIMESTAMP,
    state BOOLEAN NOT NULL
);
```

## 7.4.4.2
```
INSERT INTO task (title, detail, deadline, state) VALUES ('買い物', 'スーパーで野菜を買う', '2025-06-05 18:00:00', false);
```

```
INSERT INTO task (title, detail, deadline, state) VALUES
('掃除', '部屋の掃除をする', '2025-06-03 10:00:00', false),
('レポート作成', '学校の課題レポートを書く', '2025-06-04 23:59:00', false),
('本を読む', '技術書の第3章まで読む', '2025-06-06 20:00:00', true);
```

## 7.4.4.3
```
SELECT * FROM task;
```

```
SELECT id, title FROM task WHERE id=4;
```

```
SELECT * FROM task
WHERE
  id=2 OR 
  deadline > '2025-06-06 00:00:00';
```

## 7.4.4.4
```
UPDATE task
SET title = '図書館へ行く',
    deadline = '2025-06-07 14:00:00'
WHERE id = 2;
```

## 7.4.4.5
```
DELETE FROM task
WHERE id = 3;
```

## 7.4.4.6
```
CREATE TABLE mytable (
    id INT,
    msg VARCHAR(256)
);
```

```
DROP TABLE mytable;
```

## 7.4.5
・顧客テーブル（主キーを設定し、参照される側のテーブル）
```
CREATE TABLE customers (
    customer_id INT PRIMARY KEY,
    name VARCHAR(100)
);
```

・注文テーブル（外部キーを設定し、顧客テーブルを参照するテーブル）
```
CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    customer_id INT,
    product VARCHAR(100),
    -- 外部キーの設定
    FOREIGN KEY (customer_id) REFERENCES customers(customer_id)
);
```

・顧客テーブルへデータ登録
```
INSERT INTO
    customers (customer_id, name) 
VALUES 
    (1, '田中'),
    (2, '伊藤'),
    (3, '中島');
```

・注文テーブルへデータ登録
```
INSERT INTO
    orders (order_id, customer_id, product) 
VALUES 
    (1001, 1, 'ノートパソコン'),
    (1002, 1, 'プリンター'),
    (1003, 2, 'マウス');
```

## 7.4.6
・複数テーブルを参照するSQL
```
SELECT
    orders.order_id,
    customers.name,
    orders.product
FROM
    orders
INNER JOIN customers
    ON orders.customer_id = customers.customer_id;
```

## 7.4.7.1
・SQL
```
SELECT * FROM orders
ORDER BY order_id DESC;
```

## 7.4.7.2
・SQL
```
SELECT 
    order_id AS 注文ID, 
    customer_id AS 顧客ID, 
    product AS 商品 
FROM orders;
```

## 7.4.7.3
・SQL
```
SELECT * FROM orders
LIMIT 2;
```

## 7.4.7.4
・SQL
```
SELECT customer_id, COUNT(*) AS 注文数
FROM orders
GROUP BY customer_id;
```

## 7.4.8
・トランザクション（更新を無かったことにする）
```
-- 変更前データの参照
SELECT * FROM orders;

-- トランザクション開始（自動Commit無効）
SET AUTOCOMMIT FALSE;

UPDATE orders SET customer_id = 3 WHERE order_id = 1002;

-- トランザクション終了（更新を無かったことにする）
ROLLBACK;

-- 変更後データの参照
SELECT * FROM orders;
```

・トランザクション（更新を確定させる）
```
-- 変更前データの参照
SELECT * FROM orders;

-- トランザクション開始（自動Commit無効）
SET AUTOCOMMIT FALSE;

UPDATE orders SET customer_id = 3 WHERE order_id = 1002;

-- トランザクション終了（更新を確定させる）
COMMIT;

-- 変更後データの参照
SELECT * FROM orders;
```

## 7.5.1
・pom.xml（追記）
```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>
```

・application.properties（追記）
```
# Linking Spring Data JPA to H2
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
```

## 7.5.2
・Task.java（修正）
```
@Entity
public class Task {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private int id;
    private String title;
    private String detail;
    private LocalDateTime deadline;
    private boolean state; // false:未完了 true:完了

    〜以降省略〜
```

## 7.5.3
・TaskRepository.java（修正）
```
public interface TaskRepository extends JpaRepository<Task, Integer> {
}
```

・TaskRepositoryImpl.java（修正）
```
//@Repository
//public class TaskRepositoryImpl implements TaskRepository {
//    // タスクの情報を保持するリスト
//    private List<Task> tasklist = new ArrayList<>();
〜省略〜
```

・JPAの修正例
```
public interface TaskRepository extends JpaRepository<Task, Integer> {
    // JPQLを使った形式
    @Query("SELECT t FROM Task t WHERE t.title = :title")
    Task findByTitle(@Param("title") String title);

    // ネイティブSQLを使った形式
    @Query(value = "SELECT * FROM task WHERE title = :title", nativeQuery = true)
    Task findByTitleNative(@Param("title") String title);
}
```

## 7.5.4
・TaskListServiceImpl.java（修正）
```
@Service
public class TaskListServiceImpl implements TaskListService {

    〜中略〜

    /**
     * タスクの登録処理
     * @param title
     * @param detail
     * @param deadline
     * @return 処理結果のテキスト。成功時は空文字を返す。
     */
    @Override
    public String addTask(String title, String detail, String deadline) {
        // バリデーションチェック
        // タスク名は10文字より大きい、もしくは0文字の場合エラー。
        if(title.length() > 10 || title.isEmpty())
            return "タスク名は1文字以上10文字以下です";
        // タスク詳細は100文字より大きい場合エラー。
        if(detail.length() > 100)
            return "タスク詳細は100文字以下です";

        // 現在の総タスク数+1をIDとする。
        // int taskId = taskRepository.findAll().size() + 1;

        // deadlineはStringで受け取っているため、LocalDateTimeへ変換する。
        // なお引数が空文字の場合は、LocalDateTime.parse()でエラーとなるためnullを設定する。
        LocalDateTime _deadline = deadline.isEmpty() ? null : LocalDateTime.parse(deadline);

        // Taskオブジェクトへの詰め替え処理
        Task task = new Task();
        // task.setId(taskId);
        task.setTitle(title);
        task.setDetail(detail);
        task.setDeadline(_deadline);
        task.setState(false); // タスク未完了状態をセット。

        // タスクの登録処理
        taskRepository.save(task);
        return "";
    }

    /**
     * タスクの更新
     * @param task
     * @return
     */
    @Override
    public void updateTask(Task task) {
        taskRepository.save(task);
    }

    /**
     * タスクの削除
     * @param id
     */
    @Override
    public void deleteTask(int id) {
        taskRepository.deleteById(id);
    }

    /**
     * idをキーとし、タスクを検索
     * @param id
     * @return 検索結果のタスク
     */
    @Override
    public Task findTask(int id) {
        return taskRepository.findById(id)
                .orElseThrow(() -> new RuntimeException("タスクが見つからない"));
    }
}
```

## 7.6.2
・pom.xml（修正）
```
<!-- Spring Security関連 -->
<dependency>
  <groupId>org.springframework.boot</groupId>
  <artifactId>spring-boot-starter-security</artifactId>
</dependency>
<dependency>
  <groupId>org.thymeleaf.extras</groupId>
  <artifactId>thymeleaf-extras-springsecurity6</artifactId>
</dependency>
```

・login.html
```
<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org">
<head>
  <title>ログイン</title>
  <!-- Bootstrap CSS CDN -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body class="bg-light">

<div class="container">
  <div class="row justify-content-center mt-5">
    <div class="col-md-5">
      <div class="card shadow-sm">
        <div class="card-body">
          <h2 class="card-title text-center mb-4">ログイン</h2>

          <!-- エラーメッセージ -->
          <div th:if="${param.error}" class="alert alert-danger" role="alert">
            ログイン失敗しました
          </div>
          <div th:if="${param.logout}" class="alert alert-success" role="alert">
            ログアウトしました
          </div>
          <!-- 登録成功メッセージ -->
          <div th:if="${param.registered}" class="alert alert-success" role="alert">
            ユーザー登録が完了しました。ログインしてください。
          </div>

          <form th:action="@{/login}" method="post">
            <div class="mb-3">
              <label for="username" class="form-label">ユーザー名</label>
              <input type="text" class="form-control" id="username" name="username" placeholder="ユーザー名を入力"
                     required>
            </div>
            <div class="mb-3">
              <label for="password" class="form-label">パスワード</label>
              <input type="password" class="form-control" id="password" name="password" placeholder="パスワードを入力"
                     required>
            </div>
            <div class="d-grid">
              <button type="submit" class="btn btn-primary">ログイン</button>
            </div>
          </form>

          <hr>

          <div class="text-center">
            <a th:href="@{/register}" class="btn btn-link">新規ユーザー登録</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- Bootstrap JS Bundle CDN -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

・User.java
```
package com.webAppDev.tasklist.entity;

import jakarta.persistence.*;

@Entity
@Table(name = "users")
public class User {
  @Id
  @GeneratedValue(strategy = GenerationType.IDENTITY)
  private Long id;

  @Column(unique = true, nullable = false)
  private String username;

  @Column(nullable = false)
  private String password;

  private String role;

  public Long getId() {
    return id;
  }

  public void setId(Long id) {
    this.id = id;
  }

  public String getUsername() {
    return username;
  }

  public void setUsername(String username) {
    this.username = username;
  }

  public String getPassword() {
    return password;
  }

  public void setPassword(String password) {
    this.password = password;
  }

  public String getRole() {
    return role;
  }

  public void setRole(String role) {
    this.role = role;
  }
}
```

・UserRepository.java
```
package com.webAppDev.tasklist.repository;

import com.webAppDev.tasklist.entity.User;
import org.springframework.data.jpa.repository.JpaRepository;

import java.util.Optional;

public interface UserRepository extends JpaRepository<User, Long> {
  Optional<User> findByUsername(String username);
}
```

・CustomUserDetailsService.java
```
package com.webAppDev.tasklist.service;

import com.webAppDev.tasklist.repository.UserRepository;
import org.springframework.security.core.userdetails.User;
import org.springframework.security.core.userdetails.UserDetails;
import org.springframework.security.core.userdetails.UserDetailsService;
import org.springframework.security.core.userdetails.UsernameNotFoundException;
import org.springframework.stereotype.Service;

@Service
public class CustomUserDetailsService implements UserDetailsService {

  private final UserRepository userRepository;
  public CustomUserDetailsService(UserRepository userRepository) {
    this.userRepository = userRepository;
  }

  @Override
  public UserDetails loadUserByUsername(String username) throws UsernameNotFoundException {
    return userRepository.findByUsername(username)
            .map(user -> User.withUsername(user.getUsername())
                    .password(user.getPassword())
                    .roles(user.getRole())
                    .build())
            .orElseThrow(() -> new UsernameNotFoundException("ユーザーが存在しません: " + username));
  }
}
```

・LoginController.java
```
package com.webAppDev.tasklist.controller;

import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.GetMapping;

@Controller
public class LoginController {
  @GetMapping("/login")
  public String login() {
    return "login";
  }
}
```

・SecurityConfig.java
```
package com.webAppDev.tasklist.config;

import com.webAppDev.tasklist.service.CustomUserDetailsService;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;
import org.springframework.security.authentication.dao.DaoAuthenticationProvider;
import org.springframework.security.config.annotation.web.builders.HttpSecurity;
import org.springframework.security.crypto.bcrypt.BCryptPasswordEncoder;
import org.springframework.security.crypto.password.PasswordEncoder;
import org.springframework.security.web.SecurityFilterChain;

@Configuration
public class SecurityConfig {

  private final CustomUserDetailsService userDetailsService;
  public SecurityConfig(CustomUserDetailsService userDetailsService) {
    this.userDetailsService = userDetailsService;
  }

  @Bean
  public PasswordEncoder passwordEncoder() {
    return new BCryptPasswordEncoder();
  }

  // DaoAuthenticationProvider を使ってDB認証
  @Bean
  public DaoAuthenticationProvider authenticationProvider() {
    DaoAuthenticationProvider authProvider = new DaoAuthenticationProvider();
    authProvider.setUserDetailsService(userDetailsService);
    authProvider.setPasswordEncoder(passwordEncoder());
    return authProvider;
  }

  @Bean
  public SecurityFilterChain filterChain(HttpSecurity http) throws Exception {
    http
            .authorizeHttpRequests(auth -> auth
                    .requestMatchers("/login", "/register", "/h2-console/**").permitAll()
                    .anyRequest().authenticated()
            )
            .formLogin(form -> form
                    .loginPage("/login")
                    .defaultSuccessUrl("/tasklist", true)
                    .permitAll()
            )
            .logout(logout -> logout
                    .logoutSuccessUrl("/login?logout")
                    .permitAll()
            );

    // H2コンソール用設定
    http.csrf(csrf -> csrf.disable());
    http.headers(headers -> headers.frameOptions(frame -> frame.disable()));

    return http.build();
  }
}
```

## 7.6.3
・usersテーブル作成のSQL
```
CREATE TABLE users (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(255) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL,
    role VARCHAR(255)
);
```

## 7.6.4
・register.html
```
<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org">
<head>
  <title>ユーザー登録</title>
  <!-- Bootstrap CSS CDN -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body class="bg-light">

<div class="container">
  <div class="row justify-content-center mt-5">
    <div class="col-md-5">
      <div class="card shadow-sm">
        <div class="card-body">
          <h2 class="card-title text-center mb-4">ユーザー登録</h2>

          <!-- エラーメッセージ -->
          <div th:if="${error}" class="alert alert-danger" role="alert">
            <p th:text="${error}"></p>
          </div>

          <form th:action="@{/register}" th:object="${user}" method="post">
            <div class="mb-3">
              <label for="username" class="form-label">ユーザー名</label>
              <input type="text" class="form-control" id="username" th:field="*{username}"
                     placeholder="ユーザー名を入力" required>
            </div>
            <div class="mb-3">
              <label for="password" class="form-label">パスワード</label>
              <input type="password" class="form-control" id="password" th:field="*{password}"
                     placeholder="パスワードを入力" required>
            </div>
            <div class="d-grid">
              <button type="submit" class="btn btn-success">登録</button>
            </div>
          </form>

          <hr>

          <div class="text-center">
            <a th:href="@{/login}" class="btn btn-link">ログイン画面へ</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- Bootstrap JS Bundle CDN -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

・UserRegistrationForm.java
```
package com.webAppDev.tasklist.dto;

public class UserRegistrationForm {
  private String username;
  private String password;
  private String role; // 登録時は固定で "USER" にするのが一般的

  public String getUsername() {
    return username;
  }

  public void setUsername(String username) {
    this.username = username;
  }

  public String getPassword() {
    return password;
  }

  public void setPassword(String password) {
    this.password = password;
  }

  public String getRole() {
    return role;
  }

  public void setRole(String role) {
    this.role = role;
  }
}
```

・RegistrationController.java
```
package com.webAppDev.tasklist.controller;

import com.webAppDev.tasklist.dto.UserRegistrationForm;
import com.webAppDev.tasklist.entity.User;
import com.webAppDev.tasklist.repository.UserRepository;
import org.springframework.security.crypto.password.PasswordEncoder;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.ModelAttribute;
import org.springframework.web.bind.annotation.PostMapping;

@Controller
public class RegistrationController {

  private final UserRepository userRepository;
  private final PasswordEncoder passwordEncoder;

  public RegistrationController(UserRepository userRepository, PasswordEncoder passwordEncoder) {
    this.userRepository = userRepository;
    this.passwordEncoder = passwordEncoder;
  }

  // 登録画面表示
  @GetMapping("/register")
  public String showRegistrationForm(Model model) {
    model.addAttribute("user", new UserRegistrationForm());
    return "register";
  }

  // 登録処理
  @PostMapping("/register")
  public String registerUser(@ModelAttribute("user") UserRegistrationForm dto, Model model) {
    if (userRepository.findByUsername(dto.getUsername()).isPresent()) {
      model.addAttribute("error", "ユーザー名はすでに使われています");
      return "register";
    }

    User user = new User();
    user.setUsername(dto.getUsername());
    user.setPassword(passwordEncoder.encode(dto.getPassword())); // BCryptで暗号化
    user.setRole("USER");
    userRepository.save(user);

    return "redirect:/login?registered"; // 登録後はログイン画面へ
  }
}
```

## 7.6.5
・tasklist.html（追記）
```
</head>
<body class="bg-light">

<!-- ナビバー -->
<nav class="navbar navbar-expand-lg navbar-light bg-light shadow-sm mb-4">
    <div class="container">
        <a class="navbar-brand" href="#">タスク管理アプリ</a>
        <div class="d-flex ms-auto align-items-center">
            <span class="me-3" th:text="${#authentication.name}">ユーザー名</span>
            <form th:action="@{/logout}" method="post">
                <button type="submit" class="btn btn-outline-danger btn-sm">ログアウト</button>
            </form>
        </div>
    </div>
</nav>

<div class="container">
```

## 7.7.1
・ビルドコマンド
```
./mvnw clean package
```

・Jar実行コマンド
```
java -jar target/*.jar
```

・プロセスを探す
```
ps
```

・プロセスをキルする
```
kill {プロセスID}
```

## 7.7.2.2
・Dockerfile
```
# ===============================
# 1. ビルドステージ
# ===============================
FROM maven:3.9.9-eclipse-temurin-24 AS build

WORKDIR /app

# 依存関係キャッシュ用
COPY pom.xml .
RUN mvn dependency:go-offline -B

# ソースコードコピー
COPY src ./src

# JARをビルド
RUN mvn package -DskipTests

# ===============================
# 2. 実行ステージ（軽量）
# ===============================
FROM eclipse-temurin:24-jre-alpine

WORKDIR /app

# ビルド済みJARをコピー
COPY --from=build /app/target/*.jar app.jar

# Render用ポート設定
ENV SERVER_PORT=10000
EXPOSE 10000

# アプリ起動
ENTRYPOINT ["java", "-jar", "app.jar"]
```

・.dockerignore
```
target/
.git
.idea
```

## 7.7.2.3
・GitリポジトリへPushする
```
git init
git add .
git commit -m "first commit"
git remote add origin {URL}
git push -u origin main
```

## 7.7.3.2
・DB接続URL
```
jdbc:postgresql://{Hostname}.oregon-postgres.render.com/{Database}
```

・create文
```
CREATE TABLE task (
    id SERIAL PRIMARY KEY,
    title VARCHAR(10) NOT NULL,
    detail VARCHAR(100),
    deadline TIMESTAMP,
    state BOOLEAN NOT NULL
);
CREATE TABLE users (
    id BIGSERIAL PRIMARY KEY,
    username VARCHAR(255) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL,
    role VARCHAR(255)
);
```

## 7.7.3.3
・application.properties（修正）
```
spring.application.name=tasklist

# Enable H2 console
#spring.h2.console.enabled=true
#spring.h2.console.path=/h2-console

# Data source setup
#spring.datasource.driverClassName=org.h2.Driver
#spring.datasource.url=jdbc:h2:./h2db/taskdb
#spring.datasource.username=sa
#spring.datasource.password=12345
spring.datasource.url=jdbc:postgresql://{Hostname}/{Database}
spring.datasource.username={Username}
spring.datasource.password={Password}

# Linking Spring Data JPA to H2
#spring.jpa.database-platform=org.hibernate.dialect.H2Dialect

# Linking Spring Data JPA to PostgreSQL
spring.jpa.hibernate.ddl-auto=update
spring.jpa.database-platform=org.hibernate.dialect.PostgreSQLDialect
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```

・pom.xml（追記）
```
<!-- PostgreSQL -->
<dependency>
  <groupId>org.postgresql</groupId>
  <artifactId>postgresql</artifactId>
  <scope>runtime</scope>
</dependency>
```

・コマンド
```
git add .
git commit -m "add PostgreSQL config"
git push
```
