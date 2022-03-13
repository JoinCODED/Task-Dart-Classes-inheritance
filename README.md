# Loyal Customers 🤵‍♂️

Givin the following class:

```dart
void main() {
final customer = Customer("Khalid");
customer.add(54.5);
customer.add(12.2);
print(customer.getPurchaseAmount());
}

class Customer{
    String name;
    double purchaseAmount = 0;

    Customer(this.name);

    void add(double price){
        purchaseAmount += price;
    }

    double getPurchaseAmount() {
        return purchaseAmount;
    }
}
```

1. Set the `purchaseAmount` as private.
2. Create a class `LoyalCustomer` that extends `Customer`.
3. Create a constructor for the subclass.
4. Override the `getPurchaseAmount` to give the loyal customer a discount of 10%.
