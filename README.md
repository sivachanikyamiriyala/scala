# scala   semicolon is not mandatory 
# scala is functional and object orienited programming language 
# scala supports operator overloading 
# scala supports type infer based on the value or expression it automatically finds the type 
# scala supports bckward compactability only for source code not for binary code 
# scala supports REPL 
# scala supports statically typed programming lang we can't change the type dynamically 

val name:String = "kalyan" 

name

print(name)

scala> name
res5: String = kalyan

scala> name="xyz"
<console>:12: error: reassignment to val
       name="xyz"


var name="kalyan"

name
print(name)

name="xyz"

scala> name="xyz"
name: String = xyz

scala> name=10
<console>:12: error: type mismatch;
 found   : Int(10)
 required: String
       name=10
            ^
scala> val a=10
a: Int = 10

scala> val b=20
b: Int = 20

scala> val c=a min b
c: Int = 10

scala> val d=a max b;
d: Int = 20

examples on array : 

scala> val nums :Array[Int]=Array[Int](1,2,3,4,5) 
nums: Array[Int] = Array(1, 2, 3, 4, 5)

scala> nums
res2: Array[Int] = Array(1, 2, 3, 4, 5)

scala> val nums:Array[Int]=new Array[Int](5)
nums: Array[Int] = Array(0, 0, 0, 0, 0)

scala> nums
res3: Array[Int] = Array(0, 0, 0, 0, 0)

scala> nums(1)=20

scala> nums(0)=10

scala> nums(3)=40

scala> nums
res7: Array[Int] = Array(10, 20, 0, 40, 0)

Different ways to write array

scala> val nums:Array[Int]=Array[Int](1,2,3,4,5)
nums: Array[Int] = Array(1, 2, 3, 4, 5)

scala> nums
res8: Array[Int] = Array(1, 2, 3, 4, 5)

scala> val nums=Array[Int](1,2,3,4,5)
nums: Array[Int] = Array(1, 2, 3, 4, 5)

scala> nums
res9: Array[Int] = Array(1, 2, 3, 4, 5)

scala> val nums=Array(1,2,3,4,5)
nums: Array[Int] = Array(1, 2, 3, 4, 5)

scala> nums
res10: Array[Int] = Array(1, 2, 3, 4, 5)

scala> var nums=Array[Int](1,2,3,4,5) 
nums: Array[Int] = Array(1, 2, 3, 4, 5)

scala> nums
res11: Array[Int] = Array(1, 2, 3, 4, 5)

scala> var nums(1)=10
<console>:12: error: not found: value nums
       var nums(1)=10
           ^

scala> nums(1)=10

scala> nums
res13: Array[Int] = Array(1, 10, 3, 4, 5)

scala> nums=Array[Int](10,20)
nums: Array[Int] = [I@69afa141

scala> nums
res14: Array[Int] = Array(10, 20)


scala collections: 2 types 
 1.Immutable collections scala.collection.immutable 
 2.Mutable collections   scala.collection.mutable 

examples on range 

scala> 1 to 10 
res0: scala.collection.immutable.Range.Inclusive = Range(1, 2, 3, 4, 5, 6, 7, 8, 9, 10)

scala> 1 to 10 by 1
res1: scala.collection.immutable.Range = Range(1, 2, 3, 4, 5, 6, 7, 8, 9, 10)

scala> 10 to 1
res2: scala.collection.immutable.Range.Inclusive = Range()

scala> 10 to 1 by -1
res3: scala.collection.immutable.Range = Range(10, 9, 8, 7, 6, 5, 4, 3, 2, 1)

scala> 1 to 10 by 2
res4: scala.collection.immutable.Range = Range(1, 3, 5, 7, 9)

scala> 1 to by 3
<console>:1: error: ';' expected but integer literal found.
1 to by 3
        ^

scala> 1 to 10 by 3
res5: scala.collection.immutable.Range = Range(1, 4, 7, 10)

scala> 1 until 10
res6: scala.collection.immutable.Range = Range(1, 2, 3, 4, 5, 6, 7, 8, 9)

scala> 1 until 10 by 2
res7: scala.collection.immutable.Range = Range(1, 3, 5, 7, 9)

scala> 10 until 1 by -2
res8: scala.collection.immutable.Range = Range(10, 8, 6, 4, 2)

scala> 10 until 1 by -1
res9: scala.collection.immutable.Range = Range(10, 9, 8, 7, 6, 5, 4, 3, 2)

scala> 'a' to 'z' 
res10: scala.collection.immutable.NumericRange.Inclusive[Char] = NumericRange(a, b, c, d, e, f, g, h, i, j, k, l, m, n, o, p, q, r, s, t, u, v, w, x, y, z)

scala> 'a' to 'z' by 1
res11: scala.collection.immutable.NumericRange[Char] = NumericRange(a, b, c, d, e, f, g, h, i, j, k, l, m, n, o, p, q, r, s, t, u, v, w, x, y, z)

scala> 'a' to 'z' by 2
res12: scala.collection.immutable.NumericRange[Char] = NumericRange(a, c, e, g, i, k, m, o, q, s, u, w, y)

scala> 1.0 to 5.0 by .5
res13: scala.collection.immutable.NumericRange[Double] = NumericRange(1.0, 1.5, 2.0, 2.5, 3.0, 3.5, 4.0, 4.5, 5.0)

loops:

if(condition)
{
}

scala> for (x<- 1 to 10 by 1){print x}
<console>:12: error: missing argument list for method print in object Predef
Unapplied methods are only converted to functions when a function type is expected.
You can make this conversion explicit by writing `print _` or `print(_)` instead of `print`.
       for (x<- 1 to 10 by 1){print x}
                              ^

scala> for (x<- 1 to 10 by 1){print (x)}
12345678910
scala> for (x<- 1 to 10 by 1){println (x)}
1
2
3
4
5
6
7
8
9
10

scala> for (x<-1 to 10 ){if(x%2==0) println(x)}
2
4
6
8
10

scala> for (x<-1 to 10 ){if(x%2==1) println(x)}
1
3
5
7
9

scala> for (x<-1 to 10 if(x%2==0)){ println(x)}
2
4
6
8
10

scala> for (x<-1 to 10 if(x%2==1)){ println(x)}
1
3
5
7
9

yield improves the performance and skipping the unnecessary code


scala> for (x<- 1 to 10)yield{x}
res21: scala.collection.immutable.IndexedSeq[Int] = Vector(1, 2, 3, 4, 5, 6, 7, 8, 9, 10)

scala> for (x<- 1 to 10 )yield{if(x%2==0) x}
res22: scala.collection.immutable.IndexedSeq[AnyVal] = Vector((), 2, (), 4, (), 6, (), 8, (), 10)

scala> for (x<- 1 to 10 if(x%2==0) )yield{x}
res23: scala.collection.immutable.IndexedSeq[Int] = Vector(2, 4, 6, 8, 10)

functions:
1.anonymus functions
2.named functions
3.curried functions 

scala> (a:Int,b:Int,c:Int)=>{a+b+c}
res24: (Int, Int, Int) => Int = <function3>

scala> val name(a:Int,b:Int,c:Int)=>{a+b+c}
<console>:1: error: '=' expected but '=>' found.
val name(a:Int,b:Int,c:Int)=>{a+b+c}
                           ^

scala> val add=(a:Int,b:Int,c:Int)=>{a+b+c}
add: (Int, Int, Int) => Int = <function3>

scala> add(1,2,3)
res25: Int = 6

scala> def add(a:Int,b:Int,c:Int)={a+b+c}
add: (a: Int, b: Int, c: Int)Int

scala> add(1,2,3)
res26: Int = 6

scala> def add1(a:Int,b:Int,c:Int)={a+b+c} 
add1: (a: Int, b: Int, c: Int)Int

scala> add(1,2,3)
res27: Int = 6

scala> def add2(a:Int)(b:Int)(c:Int)={a+b+c} 
add2: (a: Int)(b: Int)(c: Int)Int

scala> add2(1)(2)(3)
res28: Int = 6

scala> def add3(a:Int,b:Int)(c:Int)={a+b+c}
add3: (a: Int, b: Int)(c: Int)Int

scala> add3(1,2)(3)
res29: Int = 6

scala> def add4(a:Int)(b:Int,c:Int)={a+b+c} 
add4: (a: Int)(b: Int, c: Int)Int

scala> add4(1)(2,3)
res30: Int = 6

scala> def factorial(num:Int)={
     | var res=1 
     | for(x<- 1 to num) {
     | res=res*x}
     | res
     | }
factorial: (num: Int)Int

scala> factorial(5)
res31: Int = 120

scala> factorial(1)
res32: Int = 1

scala> factorial(0)
res33: Int = 1

scala> val nums:Array[Int]=Array[Int](1,2,3,4,5,6)
nums: Array[Int] = Array(1, 2, 3, 4, 5, 6)

scala> nums
res34: Array[Int] = Array(1, 2, 3, 4, 5, 6)

scala> val nums:List[Int]=List[Int](1,2,3,4,5,6)
nums: List[Int] = List(1, 2, 3, 4, 5, 6)

scala> nums
res35: List[Int] = List(1, 2, 3, 4, 5, 6)

scala> val nums:Set[Int]=Set[Int](1,2,3,4,5,6)
nums: Set[Int] = Set(5, 1, 6, 2, 3, 4)

scala> nums
res36: Set[Int] = Set(5, 1, 6, 2, 3, 4)

scala> 

scala> val nums:Seq[Int]=Seq[Int](1,2,3,4,5,6)
nums: Seq[Int] = List(1, 2, 3, 4, 5, 6)

scala> nums
res37: Seq[Int] = List(1, 2, 3, 4, 5, 6)

scala> val nums:Stream[Int]=Stream[Int](1,2,3,4,5,6)
nums: Stream[Int] = Stream(1, ?)

scala> nums
res38: Stream[Int] = Stream(1, ?)

scala> val nums:Vector[Int]=Vector[Int](1,2,3,4,5,6)
nums: Vector[Int] = Vector(1, 2, 3, 4, 5, 6)

scala> nums
res39: Vector[Int] = Vector(1, 2, 3, 4, 5, 6)

scala> val nums:scala.collection.immutable.Stack[Int]=scala.collection.immutable.Stack[Int](1,2,3,4,5,6)
warning: there was one deprecation warning; re-run with -deprecation for details
nums: scala.collection.immutable.Stack[Int] = Stack(1, 2, 3, 4, 5, 6)

scala> nums
res40: scala.collection.immutable.Stack[Int] = Stack(1, 2, 3, 4, 5, 6)

scala> var nums:scala.collection.mutable.Queue[Int]=scala.collection.mutable.Queue[Int](1,2,3,4,5,6)
nums: scala.collection.mutable.Queue[Int] = Queue(1, 2, 3, 4, 5, 6)

scala> nums
res41: scala.collection.mutable.Queue[Int] = Queue(1, 2, 3, 4, 5, 6)

EXAMPLES ON LIST:

scala> var list=List[Int](3,4,5)
list: List[Int] = List(3, 4, 5)

scala> list=list:+6
list: List[Int] = List(3, 4, 5, 6)

scala> list
res46: List[Int] = List(3, 4, 5, 6)

scala> list=2+:list
list: List[Int] = List(2, 3, 4, 5, 6)

scala> list
res47: List[Int] = List(2, 3, 4, 5, 6)

scala> list=1+:list:+7
list: List[Int] = List(1, 2, 3, 4, 5, 6, 7)

scala> list
res48: List[Int] = List(1, 2, 3, 4, 5, 6, 7)

scala> val l1=List(1,2,3)
l1: List[Int] = List(1, 2, 3)

scala> val l2=List(4,5,6)
l2: List[Int] = List(4, 5, 6)

scala> l1
res49: List[Int] = List(1, 2, 3)

scala> l2
res50: List[Int] = List(4, 5, 6)

scala> val l3=l1+l2
<console>:13: error: type mismatch;
 found   : List[Int]
 required: String
       val l3=l1+l2
                 ^

scala> val l3=l1+:l2
l3: List[Any] = List(List(1, 2, 3), 4, 5, 6)

scala> val l4=l1:+l2
l4: List[Any] = List(1, 2, 3, List(4, 5, 6))

scala> val l5=l1 ::: l2
l5: List[Int] = List(1, 2, 3, 4, 5, 6)

scala> ls
<console>:12: error: not found: value ls
       ls
       ^

scala> l5
res52: List[Int] = List(1, 2, 3, 4, 5, 6) 


EXAMPLES ON MAP: 

scala> var map=Map(1->"aa",2->"bb")
map: scala.collection.immutable.Map[Int,String] = Map(1 -> aa, 2 -> bb)

scala> map=map+(3->"cc")
map: scala.collection.immutable.Map[Int,String] = Map(1 -> aa, 2 -> bb, 3 -> cc)

scala> map
res54: scala.collection.immutable.Map[Int,String] = Map(1 -> aa, 2 -> bb, 3 -> cc)

scala> map.keys
res55: Iterable[Int] = Set(1, 2, 3)

scala> map.values
res56: Iterable[String] = MapLike(aa, bb, cc)

EXAMPLES USING STRING INTERPOLATIONS 

scala> val name="kalyan"
name: String = kalyan

scala> val course="Spark"
course: String = Spark

scala> val percentage=90.5
percentage: Double = 90.5

scala> val count=100
count: Int = 100

scala> val msg1="name is :" + name + "course is :" + course + "percentage is :" + percentage + "count is :" + count
msg1: String = name is :kalyancourse is :Sparkpercentage is :90.5count is :100

scala> val msg1="name is :" + name + " ,course is :" + course + " ,percentage is :" + percentage + ", count is :" + count
msg1: String = name is :kalyan ,course is :Spark ,percentage is :90.5, count is :100

scala> val msg2="name is $name,course is $course ,percentage is $percentage count is $count "
msg2: String = "name is $name,course is $course ,percentage is $percentage count is $count "

scala> val msg2=s"name is $name,course is $course ,percentage is $percentage count is $count "
msg2: String = "name is kalyan,course is Spark ,percentage is 90.5 count is 100 "

scala> val msg2=f"name is $name,course is $course ,percentage is $percentage count is $count "
msg2: String = "name is kalyan,course is Spark ,percentage is 90.5 count is 100 "







