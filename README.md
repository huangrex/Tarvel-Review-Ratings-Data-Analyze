---
tags: homework
---
# Tarvel Review Ratings Data Set
>詳細在jupyter notebook
>
[source](https://archive.ics.uci.edu/ml/datasets/Tarvel+Review+Ratings)

## Data preprocessor
1. 發現category 11有一個元素長得很奇怪（2/t2），所以經過搜尋後把他的直替換成2
2. 把有NAN的元素給替換掉

## Data Analyze
1. 會不會有人沒有評分，然後把評分算持0->沒有
2. 分佈圖
3. 算各個feature的相關性

## Target
觀察圖形之後，可以發現Category 24有類似的圖形波動。假設人都會有習慣性，以及一些愛屋及烏的特性，例如喜歡A和B的就會比較喜歡C。以此為基準點，去計算與預測所有人對於beaches(Category 4)的喜好程度。算好之後，測試是否有scalability。

測試Dicision Tree for Category 4
### improvement
以Random forest, cross validatoin為個進一部的分析，希望降低overfitting

測試scalability發現，結果很符合預期
![](https://i.imgur.com/BbFjrX3.png)

