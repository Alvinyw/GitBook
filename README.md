# GitBook：借助 gitbook 工具创建一本书

## 创建步骤
### 1. 安装 [Node.js](https://nodejs.org/en/) 和 npm (Node.js 的安装包一般会包含 npm 的安装)；
### 2. 创建 gitbook 文件夹，并进到该文件夹：

   ```javascript
   $ mkdir /PATH/TO/gitbook
   $ cd /PATH/TO/gitbook
   ```
### 3. 安装 gitbook ：
   
   ```javascript
   $ npm install gitbook-cli --save-dev
   ```
   一般不建议将插件安装全局；
### 4. 创建你的书：
   
   ```javascript
   $ gitbook init
   ```
   上述命令行是会报错的，因为你的插件不是装在全局的；这时可用下面的命令行：
   ```javascript
   $ .\node_modules\.bin\gitbook init
   ```
   但是据我测试过，就算是把插件全局安装，最上面的 init 命令行也是会报错的，我猜想是因为我把 Node.js 装在了 C 盘了，然后 gitbook   的文件夹有读写权限，所以报错了。
   
   但我没把 Node.js 卸了重装，因为已经装了太多应用用到了 Node.js ，我怕卸了之后连这些应用也都要重装，这就太废劲了~..~
   
   init 成功之后会看到文件： `README.md` 和 `SUMMARY.md`。
### 5. 打开并编辑书目录文件 SUMMARY.md ：
    
   ```javascript
    * [Introduction](README.md)
	* [第一章：如何造火箭](ch1/build.md)
		* [1. 燃料学](ch1/fuel.md)
		* [2. 空气动力学](ch1/air.md)
		* [3. 总装工程学](ch1/enginer.md)
		* [小结](ch1/WRAPUP.md)
	* [第二章：如何回收火箭](ch2/recycle.md)
		* [1. 自动控制原理](ch2/ac.md)
		* [2. 二次利用要点](ch2/key.md)
		* [3. 三次利用要点](ch2/three.md)
		* [4. 四次利用要点](ch2/four.md)
	* [结束](end/SUMMARY.md)
   ```
   保存之后再执行下面的命令：
   
   ```javascript
   $ .\node_modules\.bin\gitbook init
   ```
   你会发现 gitbook 为你建好了 ch1、ch2、end 三个文件夹，且把在 SUMMARY.md 列出来的 md 文件都建好放在了相应文件夹里。
   
   接下来我们只要对应的打开 md 文件填写我们的内容就好。
### 6. 预览一下书的样子：
   
   ```javascript
   $ .\node_modules\.bin\gitbook serve
   ```
   执行成功之后会看到一个网址：
   
   ```javascript
   http://localhost:4000
   ```
   拷贝该网址在浏览器打开就可以预览书的样式了。
### 7. 将 md 文件 build 成 html 文件：
   
   ```javascript
   $ .\node_modules\.bin\gitbook build
   ```
   执行成功之后你会看到多了一个 **_book** 文件夹，里面就是转换好的 html 文件。
### 8. 我在 fitboog.io 上创建的 book
   [gitbook](https://alvinyw.gitbooks.io/mygitbook/content/)
   
   