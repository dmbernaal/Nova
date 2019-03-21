# Nova V1.00
Experimental Deep Learning Algorithm for Trading. Doesn't mimic real market representation so mainly for educational and experimental purposes.

## Intuition
People like to think **intuitively** when viewing trading charts. Many seasons traders cannot explain how or why they make their decisions (something scene with many areas of expertise). We aim to model just that by using **2D chart data** in the same fashion as viewing charts.

### Features
*  **Open Price**
*  **Close Price**
*  **MA5**
*  **MA10**
*  **MA20**

### Initial Labeling Method
For **Labeling** we perform a **Sliding Window Approach**

We will model **15 days** to create an image, and label accordingly: 

```python
if open_price_20th_day > close_of_15th_by_2_percent:
    prediction = "buy" # buy on 15th, sell on 20th

if open_price_20th_day < close_of_15th_by_1_percent:
    prediction = "sell" # sell on 15th, buy on 20th 

else:
    prediction = "hold"
```

### Future Work
We will experiment with different **Labeling** Methods along with other **Features** 
