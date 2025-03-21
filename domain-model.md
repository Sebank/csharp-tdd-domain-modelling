#Domain Models In Here

```
As a supermarket shopper,
So that I can pay for products at checkout,
I'd like to be able to know the total cost of items in my basket.
```

| Classes         | Methods                                     | Scenario                    | Outputs |
|-----------------|---------------------------------------------|-----------------------------|---------|
| `Basket`		  | `sumOfItems()`								| Sum price of items in basket| float   |
| `Basket`		  | `addItem(string item, int price)`			| Adds item to basket         | void    |

```
As an organised individual,
So that I can evaluate my shopping habits,
I'd like to see an itemised receipt that includes the name and price of the products
I bought as well as the quantity, and a total cost of my basket.
```

| Classes         | Methods                                     | Scenario									| Outputs					 |
|-----------------|---------------------------------------------|-------------------------------------------|----------------------------|
| `Basket`        | `checkOut(out float price)`                 | List of bought items, with duplicates     | List<Tuple<string, int>>   |

```
As a supermarket shopper,
So that I can restock my cupboards,
I want to add products into my basket.

As a supermarket shopper,
So that I can pay for products at checkout,
I'd like to be able to know the total cost of items in my basket.
```

| Classes  | Members                                                            | Methods                          | Scenario                                                   | Outputs |
|----------|--------------------------------------------------------------------|----------------------------------|------------------------------------------------------------|---------|
| `Basket` | `HashMap<String, int> items` (key is product name, value is price) | `add(String product, int price)` | Item with the provided name *is not* already in the basket | true    |
|          |                                                                    |                                  | Item with the provided name *is* already in the basket     | false   |
|          |                                                                    | `total()`                        |                                                            | int     |
