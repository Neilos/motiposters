MotiPosters
-----------

This application uses the Stripe payment system. It is written in Ruby 1.9.3 and uses the Rails 4 framework. The database is PostgreSQL.

This app requires the set up of two environment variables
* 'STRIPE_PUBLISHABLE_KEY' - containing your stripe publishable key (available from Stripe)
* 'STRIPE_SECRET_KEY' - containing your stripe secret key (available from Stripe)

If your postgreSQL database has a username and password, add the following environment variables:
* 'PG_USER' - containing your PostgreSQL username
* 'PG_PASS' - containing you PostgreSQL password
If you do not have a username and password you do not need to set up these environment variables.

The project uses paperclip which requires the installation of imagemagick (http://www.imagemagick.org/script/index.php). If using Mac OSX and homebrew install with the following command
brew install ImageMagick

Run the test suite in the command line by entering
rspec
