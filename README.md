import java.util.HashMap;

public class WordCount {
    public static void main(String[] args) {
        String str = "This is a sample string to demonstrate the word count program using HashMap";
        
        // Remove leading and trailing whitespaces
        str = str.trim();
        
        // Split the string into words
        String[] words = str.split("\\s+");

        // Create a HashMap to store word counts
        HashMap<String, Integer> wordCountMap = new HashMap<>();

        // Count the occurrences of each word
        for (String word : words) {
            // Convert the word to lowercase to ensure case-insensitive counting
            word = word.toLowerCase();
            // Update the count in the HashMap
            wordCountMap.put(word, wordCountMap.getOrDefault(word, 0) + 1);
        }

        // Display the word count
        System.out.println("Word count:");
        for (String word : wordCountMap.keySet()) {
            System.out.println(word + ": " + wordCountMap.get(word));
        }
    }
}
