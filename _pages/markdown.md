---
permalink: /markdown/
title: "Markdown"
author_profile: true
redirect_from: 
  - /md/
  - /markdown.html
---
## Code
### Python
最好用的id交叉函数
```python
def cross_match(array_1,array_2):
    array1 = array_1
    array2 = array_2
    # 构建哈希表
    hash_table = {}
    for i, num in enumerate(array1):
        if num not in hash_table:
            hash_table[num] = [i]
        else:
            hash_table[num].append(i)

    cross1 = []
    x=0
    cross2 = []
    for num in tqdm(array2):
        if num in hash_table:
            cross1.extend(hash_table[num])
            if len(hash_table[num])>1:
                cross2.extend([x for _ in range(len(hash_table[num]))] )
            else :
                cross2.extend([x])
        x=x+1
    return cross1,cross2
```

星表交叉
```python
import astropy
from astropy.coordinates import SkyCoord
from astropy import units as u

ra1=xianglk[1].data['ra'][index2]/24*360
dec1=xianglk[1].data['dec'][index2]
ckepler = SkyCoord(ra=ra1*u.degree, dec=dec1*u.degree)
clamo = SkyCoord(ra=check[1].data['ra']*u.degree, dec=check[1].data['dec']*u.degree)
idx1,idx2,sep2d,dist3d=astropy.coordinates.search_around_sky(clamo, ckepler, seplimit=3*u.arcsec, storekdtree='kdtree_sky')
```
天文间距计算
```python
c1new=SkyCoord(ra=DR7['RA'][newidx11]*u.degree, dec=DR7['DEC'][newidx11]*u.degree)
c2new=SkyCoord(ra=DR7['RA'][newidx1]*u.degree, dec=DR7['DEC'][newidx1]*u.degree)
sep=c1new.separation(c2new)
sep=sep.to(u.arcsecond)/u.arcsecond
```


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

