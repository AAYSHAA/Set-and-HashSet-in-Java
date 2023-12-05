# Set-and-HashSet-in-Java
 Below are detailed notes with code explanations for the provided Java tutorial on sets and hash sets

import java.util.HashSet;
import java.util.Set;

public class SetExample {

    public static void main(String[] args) {
        // Creating a set of strings
        Set<String> names = new HashSet<>();

        // Adding elements to the set
        names.add("Walter");
        names.add("Jesse");
        names.add("Schuyler");
        names.add("Mike");
        names.add("Saul");

        // Printing the set
        System.out.println("Initial set: " + names); // Initial set: [Mike, Jesse, Walter, Saul, Schuyler]

        // Adding a duplicate element (no effect as sets do not allow duplicates)
        names.add("Walter");

        // Printing the set after adding a duplicate
        System.out.println("Set after adding a duplicate: " + names); // Set after adding a duplicate: [Mike, Jesse, Walter, Saul, Schuyler]

        // Removing an element from the set
        names.remove("Walter");

        // Printing the set after removal
        System.out.println("Set after removing 'Walter': " + names); // Set after removing 'Walter': [Mike, Jesse, Saul, Schuyler]

        // Checking if the set contains an element
        System.out.println("Does the set contain 'Saul'? " + names.contains("Saul")); // Does the set contain 'Saul'? true

        // Getting the size of the set
        System.out.println("Size of the set: " + names.size()); // Size of the set: 4

        // Checking if the set is empty
        System.out.println("Is the set empty? " + names.isEmpty()); // Is the set empty? false

        // Clearing all elements from the set
        names.clear();

        // Printing the set after clearing
        System.out.println("Set after clearing: " + names); // Set after clearing: []

        // Adding elements to the set again
        names.add("Walter");
        names.add("Jesse");
        names.add("Schuyler");
        names.add("Mike");
        names.add("Saul");

        // Iterating through the set using an enhanced for loop
        System.out.println("Iterating through the set with an enhanced for loop:");
        for (String name : names) {
            System.out.println(name); 
            // Walter
            // Jesse
            // Schuyler
            // Mike
            // Saul
        }

        // Using a lambda expression to iterate through the set
        System.out.println("Iterating through the set with a lambda expression:");
        names.forEach(System.out::println);
        // Walter
        // Jesse
        // Schuyler
        // Mike
        // Saul

        // Using an iterator to iterate through the set
        System.out.println("Iterating through the set using an iterator:");
        java.util.Iterator<String> namesIterator = names.iterator();
        while (namesIterator.hasNext()) {
            System.out.println(namesIterator.next());
            // Walter
            // Jesse
            // Schuyler
            // Mike
            // Saul
        }

        // Creating a list with duplicates
        java.util.List<Integer> numberList = new java.util.ArrayList<>();
        numberList.add(1);
        numberList.add(2);
        numberList.add(3);
        numberList.add(2);
        numberList.add(1);

        // Creating a set to remove duplicates
        java.util.Set<Integer> numberSet = new HashSet<>(numberList);

        // Printing the set without duplicates
        System.out.println("Set without duplicates: " + numberSet); // Set without duplicates: [1, 2, 3]

        // Using a TreeSet to maintain natural ordering
        java.util.Set<String> treeSet = new java.util.TreeSet<>(names);
        System.out.println("TreeSet with natural ordering: " + treeSet); 
        // TreeSet with natural ordering: [Jesse, Mike, Saul, Schuyler, Walter]

        // Using a LinkedHashSet to maintain insertion order
        java.util.Set<String> linkedHashSet = new java.util.LinkedHashSet<>(names);
        System.out.println("LinkedHashSet with insertion order: " + linkedHashSet); 
        // LinkedHashSet with insertion order: [Walter, Jesse, Schuyler, Mike, Saul]
    }
}

