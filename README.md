# SeleniumTestAutomationOnFirefox

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.firefox.FirefoxProfile;

public class PrivateBrowsing {

    public static void main(String args[]){
        createFirefoxInstance();
    }

    public static WebDriver createFirefoxInstance(){
        FirefoxProfile firefoxProfile = new FirefoxProfile();
        firefoxProfile.setPreference("browser.private.browsing.autostart",true);
        WebDriver driver = new FirefoxDriver(firefoxProfile);
        driver.get("http://www.google.com");
        return  driver;
    }
}
