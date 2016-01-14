# XDebug是什么

XDebug是一个开放源代码的PHP程序调试器(即一个Debug工具)，可以用来跟踪，调试和分析PHP程序的运行状况。

# 安装XDebug
下载站点 http://www.xdebug.org/ 如何知道下载哪个版本，可以将执行phpinfo()输出的信息，复制到http://www.xdebug.org/find-binary.php中提交，然后xdebug会输出一段summary告诉你如何操作。我使用的操作系统是OS X EI Capitan 10.11.2,输出如下：
***
Summary

Xdebug installed: no  
Server API: FPM/FastCGI  
Windows: no  
Zend Server: no  
PHP Version: 5.4.43  
Zend API nr: 220100525  
PHP API nr: 20100525  
Debug Build: yes  
Thread Safe Build: no  
Configuration File Path: /usr/local/etc/php/5.4  
Configuration File: /usr/local/etc/php/5.4/php.ini  
Extensions directory: /usr/local/Cellar/php54/5.4.43_2/lib/php/extensions/debug-non-zts-20100525  

Instructions

1、Download xdebug-2.4.0rc3.tgz  
2、Unpack the downloaded file with tar -xvzf xdebug-2.4.0rc3.tgz  
3、Run: cd xdebug-2.4.0rc3  
4、Run: phpize (See the FAQ if you don't have phpize.  

As part of its output it should show:

Configuring for:  
...  
Zend Module Api No:      20100525  
Zend Extension Api No:   220100525  

If it does not, you are using the wrong phpize. Please follow this FAQ entry and skip the next step.  

5、Run: ./configure  
6、Run: make
7、Run: cp modules/xdebug.so /usr/local/Cellar/php54/5.4.43_2/lib/php/extensions/debug-non-zts-20100525
8、Edit /usr/local/etc/php/5.4/php.ini and add the line
zend_extension = /usr/local/Cellar/php54/5.4.43_2/lib/php/extensions/debug-non-zts-20100525/xdebug.so
9、Restart the webserver
***

按照提示，先下载xdebug的压缩文件。解压、编译、将生成的扩展文件复制到扩展文件路径、重启web服务器。  
注：/usr/local/Cellar/php54/5.4.43_2/lib/php/extensions/debug-non-zts-20100525 不同的PHP版本路径不同。

查看phpinfo(),可以看到xdebug扩展的相关信息。





