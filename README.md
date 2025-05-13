# Assignment 1: Design Your Own Class

class Smartphone:
    def __init__(self, brand, model, storage):
        self.brand = brand
        self.model = model
        self.storage = storage

    def power_on(self):
        print(f"{self.brand} {self.model} is now ON.")

    def power_off(self):
        print(f"{self.brand} {self.model} is now OFF.")

    def info(self):
        print(f"Smartphone Info: {self.brand} {self.model}, {self.storage}GB")

# Inherited class with polymorphism
class Smartwatch(Smartphone):
    def __init__(self, brand, model, storage, strap_type):
        super().__init__(brand, model, storage)
        self.strap_type = strap_type

    def info(self):  # Polymorphism: method overridden
        print(f"Smartwatch Info: {self.brand} {self.model}, Strap: {self.strap_type}")


# Activity 2: Polymorphism Challenge

class Vehicle:
    def move(self):
        print("This vehicle moves in some way.")

class Car(Vehicle):
    def move(self):
        print("Driving 🚗")

class Plane(Vehicle):
    def move(self):
        print("Flying ✈️")

class Boat(Vehicle):
    def move(self):
        print("Sailing 🚤")


# === TESTING BOTH ASSIGNMENTS ===

# Assignment 1 Testing
print("📱 Smartphone Classes:")
phone = Smartphone("Samsung", "Galaxy S21", 128)
watch = Smartwatch("Apple", "Watch Series 7", 32, "Silicone")

phone.info()
watch.info()
phone.power_on()
watch.power_off()

# Activity 2 Testing
print("\n🚗 Vehicle Polymorphism:")
vehicles = [Car(), Plane(), Boat()]
for v in vehicles:
    v.move()
