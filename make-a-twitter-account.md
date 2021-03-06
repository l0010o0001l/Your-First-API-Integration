# Make a Twitter account
Now we can move on to tweeting your horoscope message. We'll first set up your Twitter account, and then discuss authentication and making POST requests with HTTParty.

![](/assets/Screen Shot 2017-03-30 at 9.15.32 PM.png)

* If you don't already have a Twitter account or don't want to post horoscopes on your existing account, create a new Twitter account at [https://twitter.com/signup](https://twitter.com/signup) \(don't worry about picking a perfect username, it can be changed later\).

* **Note**: if you've created a Twitter account before, you won't be allowed to use the same phone number to sign up for a new account. You can sign up for a free phone number at [https://www.google.com/voice](https://www.google.com/voice)  
  that will forward to your existing number.

* If you would like, this is a good time to go to your account settings and turn off mobile and email notifications.

* Visit [https://apps.twitter.com/app/new](https://apps.twitter.com/app/new) to create a new Twitter application for this account. This will give us credentials that will allow our Sinatra app to tweet on this account's behalf.

Note: The information you enter here won't be used by the app, but make sure the \(arbitrary\) website you enter begins with "http."

* Once you have created an application for your account, visit the **Keys and Access Tokens** section.
* Create a new access token.

Leave this page open, we'll come back to it in the chapter on environment variables.

# What did we just do?

Twitter needs to give your app permission to post tweets via its API. Like many services, Twitter uses OAuth to grant that permission. Instead of just authenticating with your username and password, which could compromise your account if stolen, OAuth allows you to generate tokens that you can turn off or set to "read only."

OAuth can be a little complicated to set up, but most of that process is taken care of us by the oauth gem. You can read more about OAuth [here](http://oauth.net/).

