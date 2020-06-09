一个将json转为Google  Protocol Buffers的脚本，需要提前生成.proto文件

•同时支持 proto2 和 proto3

•支持的数据类型

•基本数据类型（整数、浮点数、布尔、字节数组）

•repeated（数组）、proto2 中的可选（optional） 、必填（required）

•extensions（proto2）、Any（proto3）

•枚举、Map、 Oneof、timestamp、duration

•嵌套的message

## 使用方法

下载protoc，并配置到环境变量后，使用

protoc --python_out=out_path proto_file_path

编译.proto文件，编译器将读取文件.proto文件，生成_pb2.py文件

target = dict2pb(cls,json_dic)

cls为_pb2.py文件中message主类，json_dic为读取的json。
