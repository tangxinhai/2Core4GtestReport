# 2Core4GtestReport

* **Bid Ask Spread(BAS)**：用于衡量买单价和卖单价的价差

$$
BAS= \frac{OfferPrice_0}{BidPrice_0}-1
$$

* **Weighted Averaged Price(WAP)**：加权平均价格

$$
WAP= \frac{BidPrice_0 \ast OfferOrderQty_0+OfferPrice_0 \ast BidOrderQty_0}{BidOrderQty_0+OfferOrderQty_0}
$$

* **Depth Imbalance(DI)**：深度不平衡

$$
DI_j=\frac{BidOrderQty_j-OfferOrderQty_j}{BidOrderQty_j+OfferOrderQty_j},j=0..9
$$

* **Press**：买卖压力指标

$$
w_i= \frac{WAP \div (Price_i-WAP)}{\sum_{j=0}^9 WAP \div (Price_j-WAP)}
$$

$$
BidPress=\sum_{j=0}^9 BidOrderQty_j \cdot w_j
$$

$$
AskPress=\sum_{j=0}^9 OfferOrderQty_j \cdot w_j
$$

$$
Press=\log (BidPress)-\log (AskPress)
$$
