MotiPosters
===========

This application is written in Ruby 1.9.3 and uses the Rails 4 framework. 

### Database Configuration
The database used by this application is PostgreSQL. If your postgreSQL database has a username and password, add the following environment variables:
* `PG_USER` - environment variable containing your PostgreSQL username
* `PG_PASS` - environment variable containing you PostgreSQL password

(If you do not have a username and password you do not need to set up these environment variables.)

### Stripe Payment Processing
This application uses the Stripe payment system and requires the set up of two environment variables
* `STRIPE_PUBLISHABLE_KEY` - environment variable containing your stripe publishable key (available from Stripe)
* `STRIPE_SECRET_KEY` - environment variable containing your stripe secret key (available from Stripe)


### Mail Configuration
The project uses ActionMailer smtp to notify users of their orders. You need to configure your own email address from which emails will be sent. It is suggested that you use a gmail account, and enter the appropriate gmail pass code in an environment variable, which is used by this application:
* `MOTIPOSTER_GMAIL_PASS`

If you wish to configure ActionMailer differently, adjust the appropriate settings in the development.rb, production.rb and test.rb.

### Paperclip and image uploading
The project uses paperclip which requires the installation of imagemagick (http://www.imagemagick.org/script/index.php). If using Mac OSX and homebrew install with the following command:

`brew install ImageMagick`

##### Test
The 'test' environment paperclip is configured to just put and retrieve images from the 'public/images/products' directory.

##### Development
In the 'development' environment paperclip is configured to put and retrieve images in a nested directory structure within the 'public/images/products' directory.

##### Production
In the 'production' environment paperclip is configured to stored images in and retrieve images from a nested directory  on amazon s3. 
Production environment requires the set up of the following environment variables.
* `S3_MOTIPOSTER_SECRET_KEY_ID` - environment variable containing your Amazon S3 access_key_id
* `S3_MOTIPOSTER_SECRET_ACCESS_KEY` - environment variable containing your Amazon S3 secret_access_key

Run the test suite in the command line by entering `rspec`
