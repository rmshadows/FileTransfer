 
 ## FORKED FROM CPPAlien的文件传输助手(FileTransfer) [原项目地址](https://github.com/CPPAlien/FileTransfer)
 
 
 ### 修改:
  - 文件路径:FileTransfer/app/src/main/java/me/pengtao/filetransfer/MainActivity.java 
  
  - 修改内容:Line 125处,重写的protected void onCreate(Bundle savedInstanceState)方法中的mToolbar.setOnMenuItemClickListener:
    
    *原代码：
            
                Intent intent = new Intent();
    
                intent.setAction(Intent.ACTION_GET_CONTENT);
                    
                intent.setType("*/*");
                    
                startActivityForResult(intent, FILE_FETCH_CODE);
    
    *修改为： 
    
                Intent intent = new Intent(Intent.ACTION_GET_CONTENT);

                intent.setType("*/*");

                intent.addCategory(Intent.CATEGORY_OPENABLE);
                    
                startActivityForResult(intent,FILE_FETCH_CODE);
  
  - 解决问题:解决了‘文件传输助手’在努比亚手机上无法打开文件浏览器上传文件的问题，原默认打开手机通讯录，修改后可以选择打开方式。


# FileTransfer
![](https://github.com/CPPAlien/FileTransfer/raw/master/app/src/main/res/mipmap-xxxhdpi/ic_launcher.png)

Transfer any files from PC to your phone easily.

[![Usage Video](http://7xq276.com2.z0.glb.qiniucdn.com/filetransfer_cover1.jpg)](https://www.youtube.com/watch?v=NUNaORa1YzM)

[![](http://7xq276.com2.z0.glb.qiniucdn.com/google_play.png)](https://play.google.com/store/apps/details?id=me.pengtao.filetransfer)

**If you are banned by GFW. You can watch the video or download apk by ways below:**

Video: https://v.qq.com/x/page/x0618rp8w9x.html

APK: http://d.6short.com/transfer

### What Next
1, Two-way transfer between PC and Phone. 

2, Support plain text send.

### We Need you
If you have any ideas for this app, welcome to submit an issue. 

If you want to add some features, welcome to pull request. 

## Thanks
The idea and some code of this app are from [WifiTransfer](https://github.com/baidusoso/WifiTransfer).
Thanks for [baidusoso](https://github.com/baidusoso).

## LICENSE
```
Copyright (c) 2018 CPPAlien

Licensed under the GNU GENERAL PUBLIC LICENSE, Version 3, 29 June 2007 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    https://github.com/CPPAlien/FileTransfer/blob/master/LICENSE

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

