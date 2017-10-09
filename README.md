## Canvas 彈力小球球

### 沒什麼好說的就是練習 Canvas 的動態
------

* canvas 基本的繪圖我就不多說囉～
* 主要重點放在球球的 Animate
* 註解裡面寫的超級霹靂清楚了～
* 以下會是比較困難點的地方，我就先列出來
``` js
/** 以下分別是計算球碰到壁該反彈的動作 **/
if (posY > canvas.height - 20) { 
    vy *= -0.9;
    vx *= 0.9; 
    posY = canvas.height * 1 - 20; 
}

/** 以下是設置彈跳的 x 距離 **/
if (posX > canvas.width - 20) {
    vx *= -0.9; 
    posX = canvas.width - 20; 
}
if (posX < 20) {
    vx = Math.abs(vx) * 0.9; 
    posX = 20; 
}
```
* 另外兩個重點
``` js
posY += vy; // y軸變動位置
posX += vx; // x軸變動位置

vy += gravity; // 重力加速度
```

### 剩下的自己練功吧！！只能靠自己體會了～
