1. To set a class member as private, we will prefix it with an underscore:

```dart
class Customer{
    String name;
    double _purchaseAmount = 0;

    Customer(this.name);

    void add(double price){
        _purchaseAmount += price;
    }

    double getPurchaseAmount() {
        return _purchaseAmount;
    }
}
```

2. Create a class `LoyalCustomer` that extends `Customer`:

```dart
class LoyalCustomer extends Customer{

}
```

3. Create a constructor for the subclass.

```dart
class LoyalCustomer extends Customer{
    LoyalCustomer(name) : super(name);

}
```

4. Override the `getPurchaseAmount` to give the loyal customer a discount of 10%.

```dart
class LoyalCustomer extends Customer{
    LoyalCustomer(name) : super(name);

  @override
      double getPurchaseAmount() {
        return _purchaseAmount * 0.9;
    }

}
```

5. To test your code:

```dart
void main() {
final customer = Customer("Khalid");
customer.add(54.5);
customer.add(12.2);
  print(customer.getPurchaseAmount());

  final loyalCustomer = LoyalCustomer("Khalid");
loyalCustomer.add(54.5);
loyalCustomer.add(12.2);
  print(loyalCustomer.getPurchaseAmount());

}

class Customer{
    String name;
    double _purchaseAmount = 0;

    Customer(this.name);

    void add(double price){
        _purchaseAmount += price;
    }

    double getPurchaseAmount() {
        return _purchaseAmount;
    }
}

class LoyalCustomer extends Customer{
    LoyalCustomer(name) : super(name);

  @override
      double getPurchaseAmount() {
        return _purchaseAmount * 0.9;
    }

}
```
