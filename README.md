
# TO-DO (Maven-Application)


A Java Maven-based Todo Application that helps you manage your tasks efficiently. This application allows you to add, update, delete, and mark tasks as complete, with data persistence using MySQL database.

## Features

- **Task Management**: Add, update, and delete tasks
- **Task Status**: Mark tasks as complete or incomplete
- **Data Persistence**: All tasks are stored in a MySQL database
- **User-Friendly Interface**: Simple and intuitive GUI built with Java Swing
- **Search Functionality**: Quickly find tasks by name or description
- **Responsive Design**: Adapts to different screen sizes

## Prerequisites

Before you begin, ensure you have the following installed:

- Java Development Kit (JDK) 11 or higher
- Apache Maven 3.6.0 or higher
- MySQL Server 8.0 or higher
- Git (optional, for version control)

## Installation

1. **Clone the repository** (if you haven't already):
   ```bash
   git clone https://github.com/yourusername/Todo_Maven-application.git
   cd Todo_Maven-application
   ```

2. **Set up the MySQL database**:
   - Start your MySQL server
   - Create a new database named `todo_db`
   - Create a MySQL user with appropriate privileges or use root (not recommended for production)

3. **Configure database connection**:
   - Open `src/main/java/com/todo/util/DatabaseConnection.java`
   - Update the database URL, username, and password according to your MySQL setup

4. **Create the required table**:
   ```sql
   CREATE TABLE IF NOT EXISTS todos (
       id INT AUTO_INCREMENT PRIMARY KEY,
       title VARCHAR(255) NOT NULL,
       description TEXT,
       is_completed BOOLEAN DEFAULT FALSE,
       created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
       updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
   );
   ```

## Building the Application

1. **Build the project using Maven**:
   ```bash
   mvn clean package
   ```

2. **Run the application**:
   ```bash
   mvn exec:java
   ```
   
   Or run the generated JAR file:
   ```bash
   java -jar target/todo-application-1.0.0.jar
   ```

## Usage

1. **Adding a Task**:
   - Click the "Add Task" button
   - Enter the task title and description
   - Click "Save" to add the task

2. **Updating a Task**:
   - Select a task from the list
   - Click the "Edit" button
   - Modify the task details
   - Click "Update" to save changes

3. **Deleting a Task**:
   - Select a task from the list
   - Click the "Delete" button
   - Confirm the deletion when prompted

4. **Marking Tasks as Complete/Incomplete**:
   - Check or uncheck the checkbox next to a task to mark it as complete or incomplete

5. **Searching Tasks**:
   - Use the search bar to filter tasks by title or description

## Project Structure

```
src/
├── main/
│   ├── java/
│   │   └── com/
│   │       └── todo/
│   │           ├── Main.java               # Application entry point
│   │           ├── dao/
│   │           │   └── TodoAppDAO.java     # Data Access Object for database operations
│   │           ├── gui/
│   │           │   └── TodoAppGUI.java     # Main GUI implementation
│   │           ├── model/
│   │           │   └── Todo.java           # Todo model class
│   │           └── util/
│   │               └── DatabaseConnection.java  # Database connection utility
│   └── resources/                          # Resource files (if any)
```

## Dependencies

- **MySQL Connector/J**: For MySQL database connectivity
- **Maven**: For dependency management and build automation

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a new branch for your feature (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Built with Java Swing
- Uses MySQL for data persistence
- Maven for dependency management

## Support

For support, please open an issue in the GitHub repository or contact the maintainers.




