# Chapter 2 Building Open Source Erlang Software
# 创建一个开源的Erlang软件(software)

Most Erlang books tend to explain how to build Erlang/OTP applications, but few of them go very much in depth about how to integrate with the Erlang community doing Open Source work.<br>
Some of them even avoid the topic on purpose. This chapter dedicates itself to doing a quick tour of the state of affairs in Erlang.
<p></p>
<font color="green">
大多数的Erlang书都倾向于说明怎样去创建Erlang/OTP applications,但鲜有更深入去介绍如何与Erlang社区集成做一些开源的工作(Open Source Work).<br>
他们中甚至有人故意回避这个主题.本章节致力快速示范下如何做这些工作。
</font>
<p></p>
OTP applications are the vast majority of the open source code people will encounter.<br>
In fact, many people who would need to build an OTP release would do so as one umbrella OTP application.
<p></p>
<font color="green">
OTP applications  是人们在绝大部分的开源代码中都会遇到的。
事实上，很多需要创建OTP release的人会只是做一个伞形结构的OTP application.
</font>
<p></p>
If what you’re writing is a stand-alone piece of code that could be used by someone building a product, it’s likely an OTP application. If what you’re building is a product that stands on its own and should be deployed by users as-is (or with a little configuration), what you should be building is an OTP release. <sup>1</sup>
<p></p>
<font color="green">
如果你正在写一个用于提供给别人创建产品的独立代码库，最好是写成OTP application. 如果你创建的产品(product)是全部基于自己本身(stands on its own)并提供给用户部署的，你应该创建的是一个OTP release.
</font>
<p></p>
The main build tools supported are rebar and erlang.mk. The former is a portable Erlang script that will be used to wrap around a lot of standard functionality and add its own, while the latter is a very fancy makefile that does a bit less, but tends to be faster when it comes to compiling.<br>
 In this chapter, I’ll mostly focus on using rebar to build things, given it’s the ad-hoc standard, is well-established, and erlang.mk applications tend to also be supported by rebar as dependencies.
<p></p>
<font color="green">
最主要的支持工具是rebar 和erlang.mk. rebar是一个附带许多标准功能的便携Erlang脚本,erlang.mk则是一个很小但却可以更快编译文件的神奇makefile 文件。<br>
在本章节中，我大部分会集中在使用rebar来创建符合标准的文件，erlank.mk application也是被rebar支持的。
</font>
<p></p>
[1]The details of how to build an OTP application or release is left up to the Erlang introduction book you have at hand.
<p></p>
<font color="green">
[注1]：关于如何创建一个OTP application 或OTP release，你可以查阅其它Erlang书籍。
</font>