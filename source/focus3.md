## 電腦下棋的關鍵： Min-Max 對局搜尋與 Alpha-Beta 修剪算法

### 前言


### Min-Max 對局搜尋法

演算法： Min-Max 對局搜尋

```javascript
function minimax(node, depth, maximizingPlayer)
    if depth = 0 or node is a terminal node
        return the heuristic value of node
    if maximizingPlayer
        bestValue := -∞
        for each child of node
            val := minimax(child, depth - 1, FALSE))
            bestValue := max(bestValue, val);
        return bestValue
    else
        bestValue := +∞
        for each child of node
            val := minimax(child, depth - 1, TRUE))
            bestValue := min(bestValue, val);
        return bestValue

(* Initial call for maximizing player *)
minimax(origin, depth, TRUE)
```


### 參考文獻
* [Wikipedia:Minimax](http://en.wikipedia.org/wiki/Minimax)
* [Wikipedia:Alpha–beta pruning](http://en.wikipedia.org/wiki/Alpha-beta_pruning)

【本文由陳鍾誠取材並修改自 [維基百科]，採用創作共用的 [姓名標示、相同方式分享] 授權】

