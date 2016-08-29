python-testcontainers
=====================

python-testcontainers provides capabilities to spin up a docker containers for test purposes would that be a database, Selenium web browser or any other cotainer.

Currently available features:

- Selenium Grid containers
- Selenim Standalone containers
- MySql db container
- PostgreSQL db container


========================

Usage example:

- Selenium Standalone containers

 You can execute test scripts using Standalone Selenium Docker containers for Firefox and Chrome:

```
    def test_standalone_container(self):
        chrome = StandaloneSeleniumContainer(SeleniumImage.STANDALONE_CHROME, DesiredCapabilities.CHROME)
        with chrome:
            driver = chrome.get_driver()
            driver.get("http://google.com")
            driver.find_element_by_name("q").send_keys("Hello")
```


Contribution
------------

Run tests:

    tox -epep8
    tox -epsphinx-docs
