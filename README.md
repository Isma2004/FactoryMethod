# FactoryMethod

## **Problem:**
In a logistics system, different modes of transportation (e.g., road, sea) are used to deliver goods. The system needs a way to plan deliveries without specifying the exact classes of the objects that will be created. This ensures flexibility and scalability as new transportation methods can be added without altering existing code.

## **Solution:**
Implemented the **Factory Method Pattern**, which defines an interface for creating an object but allows subclasses to alter the type of objects that will be created. This promotes loose coupling by eliminating the need to bind application-specific classes into the code.

### **Components:**
1. **Transport Interface (`Transport.java`):** Declares the delivery method.
2. **Concrete Transport Classes (`Truck.java`, `Ship.java`):** Implement the `Transport` interface.
3. **Logistics Abstract Class (`Logistics.java`):** Declares the factory method `createTransport()`.
4. **Concrete Logistics Classes (`RoadLogistics.java`, `SeaLogistics.java`):** Override the factory method to create specific `Transport` objects.
5. **Main Class (`Main.java`):** Demonstrates the use of the Factory Method to plan deliveries.

## **Usage:**
1. **Create a Transport:** Instantiate a specific `Logistics` subclass (`RoadLogistics` or `SeaLogistics`).
2. **Plan Delivery:** Call the `planDelivery()` method, which utilizes the factory method to create and use the appropriate `Transport` object.
