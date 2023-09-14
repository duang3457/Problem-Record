# record the problem that I cannot contact with github.com in my laptop

## problem:

my laptop cannot visit github.com or repositories under GitHub

## solution:

delete all items about github in the file(host) 

the file's location: C:\Windows\System32\drivers\etc\

## PS:
sometimes we cannot clear all items about GITHUB in this file.

## Details:

In this solution,I had tried to many methods that was unuseful to solve this problem.

Finally solved, it was the host problem.

Because I had tried to log in to GitHub and added some host entries when I was in China. 

I deleted these hosts at first (I don't think so).

Just open a VPN software, in the opening process said that there are several hosts detected in the computer, help me clean up. 

When I went back to host, it was indeed missing a large portion.

Then turn off the VPN, type in the GitHub URL and it will go to solve the host problem!

so,

What is the hosts file for?

Below are the answers I searched and collated:(IN CHINESE)

(If there are new insights later, I will improve and supplement them)

(如有侵权，即刻删除)

### 01、Hosts 工作原理

Hosts 中文叫没有扩展名的系统文件，它的工作原理就是将一些常用的网址域名与其对应的 IP 地址建立一个关联“数据库”。 Hosts 就像全国星巴克店铺名单，域名就是成都这个城市的星巴克，IP地址就是成都具体的某一家星巴克。


当我们在浏览器中输入一个需要访问的网址时，系统会首先自动从 Hosts 文件中寻找对应的 IP 地址。
一旦找到，系统会立即打开对应网页，如果没有找到，则系统再会将网址提交DNS 域名解析服务器进行 IP 地址的解析。

后来随着互联网技术的发展，计算机用户增多，通过一个 Hosts 为所有Internet 主机管理一个主机文件的工作将无法进行，于是就产生了 DNS 服务器。



### 02、如何修改 Hosts 文件

Hosts文件的位置在："C:Windows\System32\Drivers\etc\hosts" ，然后用记事本打开，进行修改。

用 WinXP 和 Win7 系统修改过Hosts文件的伙伴们，应该都知道 WinXP 和Win7 系统可以直接修改 Hosts 文件。


但是 Win10 需要管理员权限才能对其进行修改。 有一个很简单的方法，那就是直接把文件从文件夹拖到桌面，然后右键记事本打开，修改保存后再拖回去就好了。Hosts 文件还有很多作用，如我们通过修改 Hosts 文件来阻止打开某些网站。


### 03 、屏蔽网站

现在有很多网站不经过用户同意就将各种各样的插件安装到你的计算机中，对于这些网站我们可以利用 Hosts 来屏蔽它。
在 Windows 系统中，127.0.0.1 就常用来作屏蔽 IP 地址。

用记事本打开 Hosts，127.0.0.1加你需要屏蔽的网站，如127.0.0.1 http://www.baidu.com ，这样就可以屏蔽百度了。


除了修改 Hosts 文件可以阻止打开某些网站，还有其他的功能。


### 04、构建映射关系

像很多公司中，都会有自己局域网，而且还会有不同的服务器提供给公司的员工使用。在访问这些服务器时，每次就需要输入难记的 IP 地址，这对员工来说相当麻烦。

因此，在 Hosts 文件中建立 IP 映射，这样通过网址也能访问局域网中本没有域名的服务器。



### 05、访问 DNS 错误的网站
有时候，因为某些原因导致 DNS 服务器无法给出正确的 IP 地址，可以通过 Hosts 来代劳。一般我们访问网页都是通过 DNS 解析 IP 地址，如果使用本地 Hosts 则可以跳过这一步直接访问服务器 IP。

不过现在的 DNS 服务器响应速度都很快，一般没必要这样做。



### 06 、调试、测试网站

网站管理员经常会通过修改 Hosts 对网站进行线下调试。

网站在发布一些新功能前，网站管理员就会在本地或局域网，对网站进行线下测试，没有问题了再上线。



### 07 、过滤广告

Hosts 文件可以过滤掉一些网站广告。

像爱奇艺、优酷这些，可以通过修改 Hosts 文件的代码就可以轻而易举的过滤掉广告。


Hosts 文件功能强大，但是可能被病毒或恶意软件所利用，来阻止用户更新杀毒软件或访问特定网站，所以我们在电脑使用中需要防止 Hosts 文件被篡改。如果你的 Hosts 文件被改坏了，你可以直接删除这个文件，然后从别的电脑上复制一个 Hosts 文件过来。


