#学习git版本管理技巧
1. 创建新仓库    
 &emsp;&emsp;```git init```   
2. 添加代码到缓存区域  
   1. 全部加入  
    `git add -A`  
    2. 加入一份文件  
    `git add xx.py`
    3. 加入多分文件  
    `git add xx.py xx.py`
3. 提交代码  
    `git commit -m "上传时附带的相关信息"`
4. 切换上一个代码版本  
    `git reset "head^1"` 切换至上几个版本
5. 创建新的分支  
    `git checkout -b 分支名称`
6. 切换分支  
    `git checkout 分支名称`
7. 合并分支  
    `git merge 分支名称` 需要切换到master 或者main 主分支进行合并  
8. 取消分支合并  
    `git merge --abort` 
9. 删除分支  
    `git branch -D 分支名称`
10. 查看所有分支  
    `git branch`
    
11. 上传到相关仓库，以github为例子(已有的)  
    ```
    git remote add origin https://github.com/li2451492/donwload_hostel_information.git
    git branch -M main
    git push -u origin main
    ```

12. 上传相关仓库，新建的
    ```
    git init
    git add README.md
    git commit -m "first commit"
    git branch -M main
    git remote add origin https://github.com/li2451492/donwload_hostel_information.git
    git push -u origin main
    ```
13. git设置代理  
    ```
    git config --global https.proxy http://127.0.0.1:1080
    git config --global https.proxy https://127.0.0.1:1080
    //socke代理
    git config --global http.proxy socks5://127.0.0.1:1080
    git config --global https.proxy socks5://127.0.0.1:1080
    //只有github有代理
    git config --global http.https://github.com.proxy socks5://127.0.0.1:1080
    git config --global https.https://github.com.proxy socks5://127.0.0.1:1080
    //取消github代理
    git config --global --unset http.https://github.com.proxy
    git config --global --unset https.https://github.com.proxy
    //取消全局代理
    git config --global --unset http.proxy
    git config --global --unset https.proxy

```
