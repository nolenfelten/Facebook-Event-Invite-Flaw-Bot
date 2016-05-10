# Facebook-Event-Invite-Flaw-Bot

Facebook event's are used by ravers (<3) and promoters to bring people to the party.
There is a limit for how many invites one account can send. 

However :), if an account has there phone number verified, and you visit the event page using a spoofed Useragent on your browser to show that you are using an Android device, you can send as many events as you would like.
But you must do it manually.

Yeah, right.

Using Python and Firefox, along with the <a href="https://pypi.python.org/pypi/selenium">Selenium</a> module, this can actually be taken advantage of.



We want to use the browser webdriver, and we want to be able to send input to the text fields.
    from selenium import webdriver
    from selenium.webdriver.common.keys import Keys
    import os



Open Facebook
    print "\nOpening Facebook"
    browser.get('http://m.facebook.com')
    print "Facebook Opened"


Email variable
    print "\nSelecting Email Box"
    login = browser.find_element_by_id("email")

Enter Email
    print "Entering email"
    login.send_keys("")

Password variable
    print "\nSelecting Password box"
    login = browser.find_element_by_id("pass")

Enter Password
    print "Entering Password"
    login.send_keys("")
    
Login
    print "Logging in"
    login.send_keys(Keys.RETURN)



Ask for event page
    response = raw_input("Enter event page URL: ")

Go to the event page
    print "Going to event URL"
    browser.get(response)
