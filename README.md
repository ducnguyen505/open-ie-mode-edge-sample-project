<p align="center">
  <a href="" rel="noopener">
 <img width=auto height=200 src="https://user-images.githubusercontent.com/93514896/161900221-d8418c08-da1a-4d5c-a793-a411e1ce9fe5.png" alt="Bot logo"></a>
</p>

<h3 align="center"><b>Open IE Mode In Edge Chromium</b></h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![Platform](https://img.shields.io/badge/platform-katalon-green.svg)](https://katalon.com/)

</div>

---

## 📝 Table of Contents

- [About](#about)
- [How it works](#working)
- [Getting Started](#getting_started)

## 🎈 About <a name = "about"></a>

This is sample project use to run test with IE mode in Edge Chromium.

## 💭 How it works <a name = "working"></a>

### Guideline

To be able to run the test with IE Mode, you need to use the keyword:
```
CustomKeywords.'com.example.openIEModeEdgeBrowser.openBrowser'("https://google.com")
```

### Keyword sample:
```groovy
@Keyword
def openBrowser(String url) {
	System.setProperty("webdriver.ie.driver", DriverFactory.getIEDriverPath());
	InternetExplorerOptions edgeIe11Options = new InternetExplorerOptions();
	Map<String, Object> ops = (Map<String, Object>) edgeIe11Options.getCapability("se:ieOptions");
	ops.put("ie.edgechromium", true);
	ops.put("ie.edgepath", "C:\\Program Files (x86 \\Microsoft\\Edge\\Application\\msedge.exe");
	edgeIe11Options.setCapability("ignoreProtectedModeSettings", true);
	edgeIe11Options.setCapability("ignoreZoomSetting", true);
	WebDriver driver = new InternetExplorerDriver(edgeIe11Options);
	driver.get(url)
	DriverFactory.changeWebDriver(driver)
}
```

## 🏁 Getting Started <a name = "getting_started"></a>

Download the project to your computer and then open it with KS. You will find customKeyword openIEmodeEdgeBrowser at Keywords folder. </br>
This project already runs with IE by default in the settings so you don't need to settings anything.