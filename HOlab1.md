# COMP2068_Lab1
Lab 1 - Markdown language  

# 2 Things I Learned in the Form of Quiz Questions
1. Is the following code synchronous or asynchronous?

   ```js
   var food = fs.readFile('food.txt', 'utf8', function (err, food) {
     if (err) {
       console.log(err);
     } else {
       console.log(food);
     }
   });
   ```
   
   ## Answer: asynchronous because it uses a callback function
   
2. What is an MVC framework? Choose one of the parts and show a code example.

   This is an example of a model:
   ```java
   public class User {
    private int userID;
    private String email, password;
    private byte[] salt;

    public User(String email, String password) throws NoSuchAlgorithmException {
        setEmail(email);
        salt = PasswordGenerator.getSalt();
        this.password = PasswordGenerator.getSHA512Pwd(password, salt);        
    }

    public int getUserID() {
        return userID;
    }

    public void setUserID(int userID) {
        if(userID >= 0)
            this.userID = userID;
        else
            throw new IllegalArgumentException("User ID must be equal or greather than 0");
    }

    public String getEmail() {
        return email;
    }

    public void setEmail(String email) {        
        if(validEmail(email))
            this.email = email;
    }    

    public static boolean validEmail(String email) {
        return email.matches("^[A-Za-z0-9+_.-]+@[A-Za-z0-9.-]+$");
    }
   ```

## Answer: Model–view–controller is commonly used for developing software that divides an application into three interconnected parts:

* The model is the central component of the pattern. It expresses the application's behavior in terms of the problem domain, independent of the user interface. It directly manages the data, logic and rules of the application.
* A view can be any output representation of information, such as a chart or a diagram. Multiple views of the same information are possible, such as a bar chart for management and a tabular view for accountants.
* The third part or section, the controller, accepts input and converts it to commands for the model or view.

#  Questions I still have are...
* Is a JavaScript object **property** equivalent to a Java class **instance variable**?
* Is a JavaScript **function** equivalent to a Java **method**?

![Node version](./nodeVersion.jpg)
