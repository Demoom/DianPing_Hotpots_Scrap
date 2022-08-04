# DianPing_Scrap
This project scrap all the hotpots infoamtion of a cities in the DianPing website (like yelp in US), including Name, Adress, average price, rating, advices and so on.

It's pretty diffcult to solve the problem of Anti-Scrap Mechanism, they hide some of their words by using (refer) to their own font files, which makes catched info are not readable by computer and show '?'. Every '?' has their own unix number, which is also the index in font files. I solve this Anti-Scrap by using OCR to recognize the font and connect them with unix number, then replace the '?'.

本项目是爬取大众点评上杭州火锅店的信息（名字、地址、人均价格、各项评分、总评分、推荐菜等）。
正常爬取得到的字体不能解码，显示不能解码符号
本项目主要通过以下方法去解决
1. 从respond可以看到网站使用的字体woff文件，将他们下载下来
2. 把文件里的每一个字都写出来并通过OCR识别，获得字体编码与对应的字体
3. 把不能解码的符号换成字体编码，再通过编码找到字体，完成解码
