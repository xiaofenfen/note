## 项目中导入新的svg格式icon

1、下载svg格式并修改name 

2、打开https://icomoon.io/app/#/select 

3、FontAwesome右边选择Import to Set导入所有下载的svg格式图标

4、FontAwesome右边选择Select All或者只选择需要icon

5、选择Generate Font

6、修改name -> download 

7、文件打开解压缩 -> fonts -> 全选 ->copy到项目
(eg:E:\workspace\ump-ng-web\web\src\main\webapp\src\fonts) -> 自定义文件名
(eg:font)
后缀名不变，并在此目录下新建文件夹把下载的svg图标放进去

8、在https://icomoon.io/app/#/select/font左上方点击U+(show codes)把编号（例：e900)添加到项目css文件中
(eg:E:\workspace\ump-ng-web\web\src\main\webapp\src\css\common\_icon.scss)，如下形式:
.fa-ump-shrink:before {
  content: "\e900";
}

9、在css文件中引入font-face如下形式：
@font-face {
  font-family: 'FontAwesome';
  src: url('../fonts/font.eot?v=4.6.3');
  src: url('../fonts/font.eot?#iefix&v=4.6.3') format('embedded-opentype'), url('../fonts/font.woff?v=4.6.3') format('woff2'), url('../fonts/font.woff?v=4.6.3') format('woff'), url('../fonts/font.ttf?v=4.6.3') format('truetype'), url('../fonts/font.svg?v=4.6.3') format('svg');
  font-weight: normal;
  font-style: normal;

  .fa {
        font: normal normal normal 14px/1 FontAwesome;
        -webkit-font-smoothing: antialiased;
        font-size: 15px;
        vertical-align: middle;
    }
}

