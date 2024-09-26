---
permalink: /markdown/
title: "Markdown"
author_profile: true
redirect_from: 
  - /md/
  - /markdown.html
---
## Code
### Linux command
服务器jupyter远程连接
```markdown
jupyter notebook --no-browser --port=8889
ssh -N -f -L localhost:8892:localhost:8889 jhwang@10.3.10.160
```
当前文件夹下的fits文件数
```markdown
ls -l *.fits 2>/dev/null | wc -l  
```
挂后台运行并限制cpu使用率
```markdown
nohup cpulimit -l 1500 python newage_replenish.py > output.log 2>&1 &     
```
指定用户的后台程序
```markdown
top -u jhwang    
```

***
**Footnotes**

The footnotes in the page will be returned following this line, return to the section on <a href="#footnotes">Markdown Footnotes</a>.

