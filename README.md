using System;
using System.Text;
using System.Text.RegularExpressions;
using System.Threading;
using NUnit.Framework;
using OpenQA.Selenium;
using OpenQA.Selenium.Firefox;
using OpenQA.Selenium.Support.UI;

namespace SeleniumTests
{
    [TestFixture]
    public class JdpowerInputBhargaviJaguarXE2018
    {
        private IWebDriver driver;
        private StringBuilder verificationErrors;
        private string baseURL;
        private bool acceptNextAlert = true;

        [SetUp]
        public void SetupTest()
        {
            driver = new FirefoxDriver();
            baseURL = "https://www.katalon.com/";
            verificationErrors = new StringBuilder();
        }

        [TearDown]
        public void TeardownTest()
        {
            try
            {
                driver.Quit();
            }
            catch (Exception)
            {
                // Ignore errors if unable to close the browser
            }
            Assert.AreEqual("", verificationErrors.ToString());
        }

        [Test]
        public void TheJdpowerInputBhargaviJaguarXE2018Test()
        {
            driver.Navigate().GoToUrl("http://localhost/newfile.htm");
            driver.FindElement(By.LinkText("New Record")).Click();
            driver.FindElement(By.Name("sellername")).Click();
            driver.FindElement(By.Name("sellername")).Clear();
            driver.FindElement(By.Name("sellername")).SendKeys("Bhargavi");
            driver.FindElement(By.Name("email")).Click();
            driver.FindElement(By.Name("email")).Click();
            // ERROR: Caught exception [ERROR: Unsupported command [doubleClick | name=email | ]]
            driver.FindElement(By.Name("email")).Click();
            driver.FindElement(By.Name("email")).Clear();
            driver.FindElement(By.Name("email")).SendKeys("bhargavi@gmail.com");
            driver.FindElement(By.Name("phone")).Click();
            driver.FindElement(By.Name("phone")).Clear();
            driver.FindElement(By.Name("phone")).SendKeys("2131235645");
            driver.FindElement(By.Name("address")).Click();
            driver.FindElement(By.Name("address")).Clear();
            driver.FindElement(By.Name("address")).SendKeys("waterloo");
            driver.FindElement(By.Name("city")).Clear();
            driver.FindElement(By.Name("city")).SendKeys("kitchener");
            driver.FindElement(By.Name("make")).Click();
            driver.FindElement(By.Name("make")).Clear();
            driver.FindElement(By.Name("make")).SendKeys("jaguar");
            driver.FindElement(By.Name("model")).Click();
            driver.FindElement(By.Name("model")).Clear();
            driver.FindElement(By.Name("model")).SendKeys("xe");
            driver.FindElement(By.Name("year")).Click();
            driver.FindElement(By.Name("year")).Clear();
            driver.FindElement(By.Name("year")).SendKeys("2018");
            driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Vechile Year'])[1]/following::input[2]")).Click();
            driver.FindElement(By.LinkText("https://www.jdpower.com/Cars/2018/jaguar/xe")).Click();
            Assert.AreEqual("Select a 2018 Jaguar XE trim level (17)", driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='See less'])[1]/following::h2[1]")).Text);
        }
        [Test]
        public void TheJdpowerSearchdetailsListofDetailsTest()
        {
            driver.Navigate().GoToUrl("http://localhost/newfile.htm");
            driver.FindElement(By.LinkText("Search Record")).Click();
            Assert.AreEqual("List of Details", driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='https://www.jdpower.com/Cars/2000/Honda/Accord'])[1]/preceding::h1[1]")).Text);
        }
        [Test]
        public void TheJdpowerSearchVanithaHondaAccord2000Test()
        {
            driver.Navigate().GoToUrl("http://localhost/newfile.htm");
            driver.FindElement(By.LinkText("Search Record")).Click();
            driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='https://www.jdpower.com/Cars/2018/jaguar/xe'])[2]/following::a[1]")).Click();
            Assert.AreEqual("Select a 2000 Honda Accord Cpe trim level (1)", driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Select Trim'])[1]/following::h2[1]")).Text);
        }
        [Test]
        public void TheJdpowerInputKarthikKiaForte2010Test()
        {
            driver.Navigate().GoToUrl("http://localhost/newfile.htm");
            driver.FindElement(By.LinkText("New Record")).Click();
            driver.FindElement(By.Name("sellername")).Click();
            driver.FindElement(By.Name("sellername")).Clear();
            driver.FindElement(By.Name("sellername")).SendKeys("Karthik");
            driver.FindElement(By.Name("email")).Click();
            driver.FindElement(By.Name("email")).Clear();
            driver.FindElement(By.Name("email")).SendKeys("ka");
            driver.FindElement(By.Name("email")).SendKeys(Keys.Down);
            driver.FindElement(By.Name("email")).Clear();
            driver.FindElement(By.Name("email")).SendKeys("karthik@gmail.com");
            driver.FindElement(By.Name("phone")).Click();
            driver.FindElement(By.Name("phone")).Clear();
            driver.FindElement(By.Name("phone")).SendKeys("5544112233");
            driver.FindElement(By.Name("address")).Click();
            driver.FindElement(By.Name("address")).Clear();
            driver.FindElement(By.Name("address")).SendKeys("Tornto");
            driver.FindElement(By.Name("city")).Click();
            driver.FindElement(By.Name("city")).Clear();
            driver.FindElement(By.Name("city")).SendKeys("Ontario");
            driver.FindElement(By.Name("make")).Click();
            driver.FindElement(By.Name("make")).Clear();
            driver.FindElement(By.Name("make")).SendKeys("kia");
            driver.FindElement(By.Name("make")).SendKeys(Keys.Down);
            driver.FindElement(By.Name("make")).Clear();
            driver.FindElement(By.Name("make")).SendKeys("kia");
            driver.FindElement(By.Name("model")).Click();
            driver.FindElement(By.Name("model")).Clear();
            driver.FindElement(By.Name("model")).SendKeys("f");
            driver.FindElement(By.Name("model")).SendKeys(Keys.Down);
            driver.FindElement(By.Name("model")).SendKeys(Keys.Tab);
            driver.FindElement(By.Name("year")).Clear();
            driver.FindElement(By.Name("year")).SendKeys("2010");
            driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Vechile Year'])[1]/following::input[2]")).Click();
            driver.FindElement(By.LinkText("https://www.jdpower.com/Cars/2010/kia/Forte")).Click();
            Assert.AreEqual("Select a 2010 Kia Forte trim level (1)", driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Select Trim'])[1]/following::h2[1]")).Text);
        }
        [Test]
        public void TheJdpowerInputVanithaHondaAccord2000Test()
        {
            driver.Navigate().GoToUrl("http://localhost/newfile.htm");
            driver.FindElement(By.LinkText("New Record")).Click();
            driver.FindElement(By.Name("sellername")).Click();
            driver.FindElement(By.Name("sellername")).Click();
            driver.FindElement(By.Name("sellername")).Click();
            // ERROR: Caught exception [ERROR: Unsupported command [doubleClick | name=sellername | ]]
            driver.FindElement(By.Name("sellername")).Click();
            driver.FindElement(By.Name("sellername")).Clear();
            driver.FindElement(By.Name("sellername")).SendKeys("Vanitha");
            driver.FindElement(By.Name("email")).Click();
            driver.FindElement(By.Name("email")).Click();
            driver.FindElement(By.Name("email")).Clear();
            driver.FindElement(By.Name("email")).SendKeys("vanitha@gmail.com");
            driver.FindElement(By.Name("phone")).Click();
            driver.FindElement(By.Name("phone")).Clear();
            driver.FindElement(By.Name("phone")).SendKeys("1223546325");
            driver.FindElement(By.Name("address")).Click();
            driver.FindElement(By.Name("address")).Click();
            driver.FindElement(By.Name("address")).Clear();
            driver.FindElement(By.Name("address")).SendKeys("Mumbai");
            driver.FindElement(By.Name("city")).Click();
            driver.FindElement(By.Name("city")).Clear();
            driver.FindElement(By.Name("city")).SendKeys("andheri");
            driver.FindElement(By.Name("make")).Click();
            driver.FindElement(By.Name("make")).Clear();
            driver.FindElement(By.Name("make")).SendKeys("Honda");
            driver.FindElement(By.Name("model")).Click();
            driver.FindElement(By.Name("model")).Clear();
            driver.FindElement(By.Name("model")).SendKeys("Accord");
            driver.FindElement(By.Name("year")).Click();
            driver.FindElement(By.Name("year")).Clear();
            driver.FindElement(By.Name("year")).SendKeys("2000");
            driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Vechile Year'])[1]/following::input[2]")).Click();
            driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='https://www.jdpower.com/Cars/2018/jaguar/xe'])[2]/following::a[1]")).Click();
            Assert.AreEqual("Select a 2000 Honda Accord Cpe trim level (1)", driver.FindElement(By.XPath("(.//*[normalize-space(text()) and normalize-space(.)='Select Trim'])[1]/following::h2[1]")).Text);
        }
        private bool IsElementPresent(By by)
        {
            try
            {
                driver.FindElement(by);
                return true;
            }
            catch (NoSuchElementException)
            {
                return false;
            }
        }

        private bool IsAlertPresent()
        {
            try
            {
                driver.SwitchTo().Alert();
                return true;
            }
            catch (NoAlertPresentException)
            {
                return false;
            }
        }

        private string CloseAlertAndGetItsText()
        {
            try
            {
                IAlert alert = driver.SwitchTo().Alert();
                string alertText = alert.Text;
                if (acceptNextAlert)
                {
                    alert.Accept();
                }
                else
                {
                    alert.Dismiss();
                }
                return alertText;
            }
            finally
            {
                acceptNextAlert = true;
            }
        }
    }
}
