# TestingGit1
For testing first git programme
# mavensteps
Reminders for setting up a maven project
# myMaven
Steps to run a maven project in itellij ide
select a new project 
Then select maven
Choose a name for groupID e.g(com.learn.maven)
Choose artifactsID e.g (learn.maven)
you could tick using a template archetype or just click finish.
In our new proect go to source
Two folders main and test.
for development choose main,but for testing purposes choose test 
There is a maven pakage created already. you could use his or create another.
Create a new simple class.
Scroll down identify a file call pom.xlm(most important file for our project).
Open the xml file and yo can add dependencies we need for our project.
These dependecies can be downloaded from https://mvnrepository.com/
Then the ide will automatically update the for us.
We can share the xml updated file with our team so we are all using the same updated versions.

/////////////////////////////////////////////////////////////////////////////////

Test code to show application and browser Automation Example:
---------------------------------------------------------------
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.firefox.FirefoxDriver;

import org.testng.annotations.BeforeTest;
import org.testng.annotations.Test;

public class AccNew {
WebDriver driver;

    @BeforeTest
    public void setUp(){

        System.setProperty("webdriver.gecko.driver","C:\\Users\\lenovo\\Desktop\\drivers\\geckodriver.exe");
        WebDriver driver = new FirefoxDriver();
        driver.get("http://newtours.demoaut.com/");
        String T = driver.getTitle();
        System.out.println(T);

    }

    @Test(priority = 1)

    public void registerAcc(){
        System.out.println("Registration successful");
    }
    @Test(priority = 2)
    public void logIn(){
        System.out.println("Successfully log-in");

    }
    @Test(priority = 3)
    public void navigateMenu(){
        System.out.println("Menu navigatable");
    }
    @Test(priority = 4)
    public void accSetting(){
        System.out.println("Sucessfully access account Settings");
    }
    @Test(priority = 5)
    public void changeEmail(){
        System.out.println("Email successfully changed");
    }
    @Test(priority = 6)
    public void selectItem(){
        System.out.println("Item selected");
    }
    @Test(priority = 7)
    public void goToCheckOut(){
        System.out.println("Sucessfully checked Out");
    }

    @Test(priority = 8)
    public void signOut(){
        System.out.println("Successfully Loogged Out");
    }




}


