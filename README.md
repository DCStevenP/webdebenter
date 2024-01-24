// Name: Steven Pootoolal
// Date: 01/24/24
// App: Ice Cream Factory
// Description: Goes over 7 problems to create a ice cream app for a factory

// Problem 1: Class Design and Inheritance
class Ingredient 
{
    String name;
    int quantity;
    String expirationDate;

    public Ingredient(String name, int quantity, String expirationDate) 
    {
        this.name = name;
        this.quantity = quantity;
        this.expirationDate = expirationDate;
    }
}

class Milk extends Ingredient {
    public Milk(String name, int quantity, String expirationDate) 
    {
        super(name, quantity, expirationDate);
    }
}

class Flavor extends Ingredient {
    public Flavor(String name, int quantity, String expirationDate) 
    {
        super(name, quantity, expirationDate);
    }
}

// Problem 2: Encapsulation
class IceCream {
    private String flavor;
    private String topping;
    private double price;

    public IceCream(String flavor, String topping, double price) 
    {
        this.flavor = flavor;
        this.topping = topping;
        this.price = price;
    }

    public String getFlavor() 
    {
        return flavor;
    }

    public void setFlavor(String flavor) 
    {
        this.flavor = flavor;
    }

    public String getTopping() 
    {
        return topping;
    }

    public void setTopping(String topping) 
    {
        this.topping = topping;
    }

    public double getPrice() 
    {
        return price;
    }

    public void setPrice(double price) 
    {
        this.price = price;
    }

    public void calculatePrice() 
    {
        // Implementation of price calculation based on flavor and toppings
    }
}

// Problem 3: Interface and Polymorphism
interface ProductionProcess 
{
    void mixIngredients();

    void freeze();
}

class IceCreamMachine implements ProductionProcess 
{
    public void mixIngredients() 
    {
        // Implementation of mixing ingredients
    }

    public void freeze() 
    {
        // Implementation of freezing
    }

    public void dispense() 
    {
        // Unique method for IceCreamMachine
    }
}

class IceCreamTruck implements ProductionProcess 
{
    public void mixIngredients() {
        // Implementation of mixing ingredients
    }

    public void freeze() {
        // Implementation of freezing
    }

    public void sell() {
        // Unique method for IceCreamTruck
    }
}

// Problem 4: Composition
import java.util.ArrayList;
import java.util.List;

class IceCreamFactory 
{
    String name;
    List<IceCream> productionLine;

    public IceCreamFactory(String name) 
    {
        this.name = name;
        this.productionLine = new ArrayList<>();
    }

    public void addIceCream(IceCream iceCream) 
    {
        productionLine.add(iceCream);
    }
}

// Problem 5: Exception Handling
class IngredientManager {
    public void checkExpirationDate(Ingredient ingredient) throws IngredientExpiredException 
    
    {
        // Implementation to check expiration date
        if (/*ingredient has expired"*/) 
        {
            throw new IngredientExpiredException("Ingredient has expired!");
        }
    }
}

class IngredientExpiredException extends Exception 
{
    public IngredientExpiredException(String message) 
    {
        super(message);
    }
}

// Problem 6: Static Members
class SalesReport 
{
    static double totalSales;

    public void recordSale(double amount)
    {
        totalSales += amount;
    }
}

// Problem 7: Use Case Scenario and Documentation
/*
Use Case Scenario:
The Ice Cream Factory produces various flavors of ice cream using different ingredients. 
Ice creams are created using IceCream objects, and the production process involves mixing ingredients and freezing. 
The factory uses IceCreamMachines and IceCreamTrucks for production and selling, respectively. 
Ingredient expiration is checked by IngredientManager to ensure quality. 
Sales are recorded in the SalesReport.
*/
