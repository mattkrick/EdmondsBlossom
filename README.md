# EdmondsBlossom
Edmond's maximum weighted matching algorithm (Blossom algorithm) in O(n^3)

##Installation
`npm install edmonds-blossom --save`

##How to use
```
var blossom = require('./edmonds-blossom');
var data = [
      [0, 1, 6],
      [0, 2, 10],
      [1, 2, 5]
    ];
var results = blossom(data);
//results: [2,-1,0];
```
The results are read as follows: index 0 is matchced up with index 2. Index 1 is not used. Index 2 is matched up with index 0 (redundant information).
###What's the most basic example of a problem that this solves?
Let's assume I own a store & only sell items in groups of two.

- If I sell a PENCIL and an ERASER, I earn $3
- If I sell a PENCIL and a MARBLE , I earn $2
- If I sell a RULER and an ERASER, I earn $2

Each customer is willing to buy up to 1 item of each & I want to maximize profit. Therefore, selling #1 AND #2 is illegal because that would be 2 pencils. #1 AND #3 would is also illegal due to the erasers. So, legal moves are: only #1, only #2, only #3, or #2 AND #3. Since the last option has a profit of $5, I should do that.


