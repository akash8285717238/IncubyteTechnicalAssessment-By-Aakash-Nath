# IncubyteTechnicalAssessment-By-Aakash-Nath
package Assessment ;

import org.openqa.selenium.chrome.ChromeDriver;

//public class IncubyteTechnicalAssessment 

	

	public class MagentoAccountAutomation {

	    public static void main(String[] args) {
	        // Set the path to your chromedriver executable
	        System.setProperty("webdriver.chrome.driver", "/path/to/your/chromedriver");

	        // Initialize ChromeDriver
	        WebDriver driver = new ChromeDriver();

	        try {
	            // Open the website
	            driver.get("https://magento.softwaretestingboard.com/");

	           
	            WebElement createAccountLink = driver.findElement(By.linkText("https://magento.softwaretestingboard.com/customer/account/login/referer/aHR0cHM6Ly9tYWdlbnRvLnNvZnR3YXJldGVzdGluZ2JvYXJkLmNvbS8%2C/"));
	            createAccountLink.click();

	            WebElement signInLink = driver.findElement(By.linkText("\"https://magento.softwaretestingboard.com/customer/account/login/referer/aHR0cHM6Ly9tYWdlbnRvLnNvZnR3YXJldGVzdGluZ2JvYXJkLmNvbS8%2C/\""));
	            signInLink.click();

	            WebElement emailSignInInput = driver.findElement(By.id("(//div[@class=\"control\"])[2]"));
	            emailSignInInput.sendKeys("aakash.nath4it@gmail.com");

	            WebElement passwordSignInInput = driver.findElement(By.id("(//div[@class=\"control\"])[3]"));
	            passwordSignInInput.sendKeys("AK@Sh123456789");

	            WebElement signInButton = driver.findElement(By.xpath("(//div[@class=\"primary\"])[1]"));
	            signInButton.click();

	            // Wait for sign-in to complete (you can improve this with WebDriverWait)
	            Thread.sleep(3000);

	            System.out.println("Sign in successful!");

	        } catch (Exception e) {
	            e.printStackTrace();
	        } finally {
	            // Close the browser
	            driver.quit();
	        }
	    }
	}




