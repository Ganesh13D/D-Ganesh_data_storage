# D-Ganesh_data_storage

public class DataRepository {
    private Map<String, String> storage = new HashMap<>();

    // Store data
    public void save(String key, String value) {
        storage.put(key, value);
    }

    // Retrieve data
    public String get(String key) {
        return storage.getOrDefault(key, "Not Found");
    }

    // Delete data
    public void delete(String key) {
        storage.remove(key);
    }

    // Display all data
    public void displayAll() {
        storage.forEach((k, v) -> System.out.println(k + ": " + v));
    }

    public static void main(String[] args) {
        DataRepository repo = new DataRepository();
        repo.save("user1", "Alice");
        repo.save("user2", "Bob");
        System.out.println("Retrieve user1: " + repo.get("user1"));
        repo.displayAll();
    }
}
