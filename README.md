# Madombidzha-Rugby-Club-Management-System
Madombidzha Rugby Club Management System is a simple Java-based console application designed to help manage player information for a small, local rugby club based in Madombidzha, a community near Makhado Town in Venda, Limpopo, South Africa.
public class Player {
    private String name;
    private int age;
    private String position;

    public Player(String name, int age, String position) {
        this.name = name;
        this.age = age;
        this.position = position;
    }

    public String toString() {
        return name + "," + age + "," + position;
    }

    public static Player fromString(String line) {
        String[] parts = line.split(",");
        return new Player(parts[0], Integer.parseInt(parts[1]), parts[2]);
    }

    public void display() {
        System.out.println("Name: " + name + ", Age: " + age + ", Position: " + position);
    }
}
