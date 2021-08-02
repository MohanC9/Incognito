# Incognito


public class IncognitoBrowsing {
	static WebDriver driver = null;
	public static void main(String[] args) {
		
		DesiredCapabilities capable = DesiredCapabilities.chrome();
		ChromeOptions option = new ChromeOptions();
		option.addArguments("incognito");
		capable.setCapability(ChromeOptions.CAPABILITY, option);
		WebDriverManager.chromedriver().setup();
		driver = new ChromeDriver(capable);
		
		driver.get("https://www.spicejet.com/");
