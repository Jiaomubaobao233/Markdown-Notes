## Ruby
- Ruby Classes https://ruby-doc.org/core-2.7.1/index.html#classes
- Ruby 菜鸟教程 https://www.runoob.com/ruby/ruby-tutorial.html

## 输入
```ruby
#一行内读取一个string，删除换行符
zhongxu = gets.chomp

#一行内读取一个integer
k = gets.to_i

#一行内读取多个integer
N, M = gets.split.map{|a| a.to_i}
N, M = gets.split.map(&:to_i)

#一行内读取一个string数组
a = gets.split

#一行内读取一个integer数组
x = gets.split.map{|a| a.to_i}
x = gets.split.map(&:to_i)
```

## 建立数组
```ruby
#建立0..n-1为下标的数组
s1 =  Array.new(n)

#建立0..n-1为下标的integer数组，并初始化为0
s2 =  Array.new(n,0)

#建立0..h-1, 0..w-1为下标的二维integer数组，并初始化为0
#和python类似，要注意是否每个子数组继承了同一id
s = Array.new(h, Array.new(w, 0))

#建立0..9为下标的set数组，并初始化为包含对应的下标的字符
require 'set'
cho = Array.new(10)
for i in "0".."9" do
    cho[i.to_i] = Set.new([i])
end

#建立0..h+1为下标的string数组，并初始化为“”
#不要对元素使用<<运算符
s = Array.new(h + 2, "")

#从range建立set
require 'set'
S = (2..n).to_set
```
