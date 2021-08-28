# Shopping Basket Kata

Implement the following **user story** using Outside-in TDD, starting from an acceptance test.

**Shopping basket** <br/>
As a customer <br/>
I want to see details of items in my shopping basket <br/>
So that I can better plan my shopping strategy

```
Given I add 2 units of "The Hobbit" to my shopping basket
  And I add 5 units of "Breaking Bad"
 When I check the content of my shopping basket
 Then it should contain the following infomation:
    * Creation date (of the shopping basket)
    * 2 x The Hobbit
    * 5 x Breaking Bad
    * Total: £45.00
```

### Guidelines

Use the following specification:

```javascript
class ShoppingBasketService {
  constructor() {}
  addItem(userId: UserID, productId: ProductID, quantity: number) {}
  basketFor(userId: UserID) {}
}
```

**Available Products (this will be represented as an in-memory repository)**

- Books
  - 10001: Lord of the Rings - £10.00
  - 10002: The Hobbit - £5.00
- DVDs
  - 20001: Game of Thrones - £9.00
  - 20110: Breaking Bad - £7.00

**Some technical constraints**

- The shopping basket should be created when the first product is added.
- The shopping basket should be persisted (In-memory)
- Each user should have her own shopping basket.