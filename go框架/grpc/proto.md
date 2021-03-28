1. Optional的字段和默认值

   用optional字段修饰的变量，可以用optional int32 result_per_page = 3 [default = 10];当中的default来修饰这个值的默认值，如果没有设置default值，那设置的值就是默认值

2. 导入定义

   import "myproject/other_protos.proto";用import导入想要的文件

3. Go_package作用

   将生成的包名重命名

4. protoc命令的使用

   $ protoc --go_out=./go/ ./proto/helloworld.proto

   $ protoc --go_out=./go/ -I proto ./proto/helloworld.proto

   --go_out表示生成的是go文件，如果是java则生成的是java_out

   （1）第一个路径(./go/ )是生成的go文件的路径，第二个路径(./proto/helloworld.proto)是proto的路径文件名

   （2）第一个路径(./go/ )仍然是生成的go文件的路径，第二个路径加-I的proto是指如果helloworld.proto中有import部分，improt的搜索路径就是proto，如果没有指定搜索路径的话，就在当前目录中查找

