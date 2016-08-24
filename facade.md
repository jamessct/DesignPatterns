The Facade Design Pattern

Basically, this 'design pattern' provides a means to utilize a single method on the selected classes with different outcomes. (As far as I can determine anyway).

The facade provides "convenient methods for common tasks"

Also "makes the [software] library more readable"

1) Create interface

2) Create classes which implement the interface

3) Create a 'facade' class (not a class named facade, but a class which will be used in the implementation of the facade design pattern.  This will be a class that can create instances of the classes which are attatched to it through methods.

4) Use the facade class (obvs).

5) Profit?

--------------------------------

1) 

public interface Fruit() {
  void harvest();
}

2) 

public class Orange implements Fruit() {
  
  @Override
  public void harvest(){
    System.out.println("yum a zesty orange nice!");
  }
}

public class Banana implements Fruit() {

  @Override
  public void harvest(){
    System.out.println("what is this tasteless yellow mush")
  }
}

3) 

public class FruitHarvester() {
  private Fruit Orange();
  private Fruit Banana();

  public FruitHarvester() {
    orange = new Orange();
    banana = new Banana();
  }  

  public void harvestOrange() {
    orange.harvest();
  }

  public void harvestBanana() {
    banana.harvest();
  }
}

4)

public class HarvestingSomeFruits {
   public static void main(String[] args) {
      FruitHarvester fruitHarvester = new FruitHarvester();

      fruitHarvester.harvestOrange();
      fruitHarvester.harvestBanana();   
   }
}

5) $$$

---------------------