import java.io.File;
import java.io.PrintWriter;
import java.util.HashMap;
import java.util.Scanner;

public class Hashmap_01 {
    public static void main(String[] args) throws Exception {

    HashMap<String, Integer> hm = new HashMap<>();
    File file = new File("ECOM_DATASHEET.txt");

    Scanner sc = new Scanner(file);

    if (sc.hasNextLine()) sc.nextLine();

    while (sc.hasNextLine()) {
        String[] parts = sc.nextLine().split("\\s+");

        String product = parts[7] + " " + parts[8];
        int amount = Integer.parseInt(parts[9]);

        hm.put(product, hm.getOrDefault(product, 0) + amount);
    }
    sc.close();

    // update
    hm.put("Product E", hm.getOrDefault("Product E", 0) + 50);

    // write to new file
    PrintWriter pw = new PrintWriter(new File("UPDATED_DATA.txt"));

    for (String key : hm.keySet()) {
        pw.println(key + " " + hm.get(key));
    }

    pw.close();

    System.out.println("File updated!");
}
}
