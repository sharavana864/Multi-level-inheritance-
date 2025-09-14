# Multilevel Inheritance in Java

## Aim
To implement and demonstrate **Multilevel Inheritance** in Java using classes `Person`, `Employee`, and `Manager`.

---

## Algorithm
1. Start the program.
2. Create a **base class `Person`** with attributes:
   - `name`
   - `age`
   - Method: `displayPersonInfo()`.
3. Create a **derived class `Employee`** that extends `Person`:
   - Attributes: `employeeId`, `department`.
   - Method: `displayEmployeeInfo()`.
4. Create another **derived class `Manager`** that extends `Employee`:
   - Attribute: `teamSize`.
   - Method: `displayManagerInfo()`.
5. In the `main` method:
   - Create an object of `Manager`.
   - Assign values to all attributes (from `Person`, `Employee`, and `Manager`).
   - Call all display methods to show the details.
6. Stop the program.

---

## Code

```java
package sharavana;


class Person {
    String name;
    int age;

    void displayPersonInfo() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}


class Employee extends Person {
    int employeeId;
    String department;

    void displayEmployeeInfo() {
        System.out.println("Employee ID: " + employeeId);
        System.out.println("Department: " + department);
    }
}


class Manager extends Employee {
    int teamSize;

    void displayManagerInfo() {
        System.out.println("Team Size: " + teamSize);
    }
}

public class MultilevelInheritanceDemo {
    public static void main(String[] args) {
        Manager m = new Manager();
        m.name = "Alice";
        m.age = 35;
        m.employeeId = 101;
        m.department = "IT";
        m.teamSize = 10;

        
        m.displayPersonInfo();
        m.displayEmployeeInfo();
        m.displayManagerInfo();
    }
}
