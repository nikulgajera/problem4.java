# problem4.java
java
import java.util.HashMap;
import java.util.List;
import java.util.Map;

public class Multiples {
    public static void main(String[] args) {
        List<Integer> numbers = List.of(1, 2, 8, 9, 12, 46, 76, 82, 15, 20, 30);
        Map<Integer, Integer> counts = new HashMap<>();

        for (int i = 1; i <= 9; i++) {
            counts.put(i, 0);
        }

        for (int number : numbers) {
            for (int i = 1; i <= 9; i++) {
                if (number % i == 0) {
                    counts.put(i, counts.get(i) + 1);
                }
            }
        }

        System.out.println(counts);
    }
}
