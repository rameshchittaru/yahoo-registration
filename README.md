# yahoo-registration
give the values of date day year and gender values by using selenium webdriver


package pack;

import org.openqa.selenium.support.ui.Select;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;

public class sample {
	public static void main(String args[]){
		WebDriver driver = new FirefoxDriver();
		driver.manage().window().maximize();
		driver.get("http://edit.europe.yahoo.com/registration");
		
		WebElement month = driver.findElement(By.id("month"));
		WebElement day = driver.findElement(By.id("day"));
		WebElement year = driver.findElement(By.id("year"));
		
		Select sel = new Select(month);
		sel.selectByIndex (1);
		
		Select sel1 = new Select(day);		
		sel1.selectByIndex(9);
		
		Select sel2 = new Select (year);
		sel2.selectByIndex(20);
		
		driver.findElement(By.id("male")).click();
	}
}
		
		
		
