# AspireAssesement
AspireAssesement


package aspireassessment.aspireassessment;

import java.awt.List;

import org.openqa.selenium.By;

import org.openqa.selenium.Keys;

import org.openqa.selenium.WebDriver;

import org.openqa.selenium.WebElement;

import org.openqa.selenium.chrome.ChromeDriver;

import org.openqa.selenium.interactions.Actions;

import org.testng.annotations.Test;


public class SampleTest {
	
	@Test
public void TestAssesment() throws InterruptedException
{

		//System.setProperty("webdriver.chrome.driver", "C:\\Users\\prateek.krishna.INCOFORGETECH\\Documents\\Automation\\selenium\\chromedriver_win32\\chromedriver.exe");
				System.setProperty("webdriver.chrome.driver", "C:\\Users\\prateek.krishna.INCOFORGETECH\\Documents\\Automation\\selenium\\drivers\\chrome\\chromedriver.exe");	
				 	
				//Create driver object for chrome browser
						//Class name = ChromeDriver
						WebDriver driver = new ChromeDriver();
						
						driver.get("https://aspireapp.odoo.com");
						driver.manage().window().maximize();
						driver.findElement(By.xpath("//input[@id='login']")).sendKeys("user@aspireapp.com");
						driver.findElement(By.xpath("//input[@id='password']")).sendKeys("@sp1r3app");
						driver.findElement(By.xpath("//button[@class='btn btn-primary btn-block']")).submit();
						driver.manage().window().maximize();
						Thread.sleep(5000);
						
						driver.findElement(By.xpath("//a[@href='#menu_id=101&action_id=207']")).click();
						Thread.sleep(5000);
						
						driver.findElement(By.xpath("//ul[@class='o_menu_sections']/li[3]")).click();
						
						driver.findElement(By.xpath("//a[@href=\"#menu_id=117&action=204\"]")).click();
						
						driver.get("https://aspireapp.odoo.com/web#id=&action=204&model=product.template&view_type=form&cids=1&menu_id=101");	
//driver.findElement(By.xpath("/html[1]/body[1]/div[4]/div[1]/div[1]/div[2]/div[1]/div[1]/div[1]/button[1]")).click();
						
//driver.findElement(By.xpath("//button[contains(text(),'Create')]")).click();
						
				
						//driver.get("https://aspireapp.odoo.com/web#action=204&cids=1&menu_id=117");


						//button[@class='btn btn-primary o-kanban-button-new']
						
						  //Actions act = new Actions(driver);
						   
						   //act.sendKeys(Keys.TAB).build().perform();
						   //act.sendKeys(Keys.RETURN).build().perform();
				
						///html/body/div[4]/div/div[1]/div[2]/div[1]/div/div/button
				
						driver.findElement(By.xpath("//body[1]/div[2]/div[1]/div[2]/div[1]/div[1]/div[2]/div[4]/h1[1]/input[1]")).click();
					//driver.findElement(By.xpath("button[@class='btn btn-primary o-kanban-button-new']")).click();
	
						 
						   driver.findElement(By.xpath("//input[contains(@name, 'name')]")).sendKeys("Prateek Coforge Ltd");
						driver.findElement(By.xpath("//body[1]/div[2]/div[1]/div[1]/div[2]/div[1]/div[1]/div[1]/div[2]/button[1]")).click();
						
						
						//driver.findElement(By.xpath("//button[@name='action_update_quantity_on_hand']")).click();
						
}
}
