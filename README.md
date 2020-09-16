# **Aquaponics Shop**

This is my __Full Stack Project with Django Frameworks__. It is a webshop for Aquaponics products to built your own system.
Last project to finish Full Stack Web Developer Code Institute course. 
Live Demo: https://aquaponics-shop.herokuapp.com/

## Purpose
The purpose of the project is to build a full-stack site based around business logic used to control a centrally-owned dataset.

The site allows users to search aquaponics products by keywords, they can search by categories as well, and after registration/login they can purchase the products.

The project has the following sections:

## Features

### Home page
Contains a background image with bubbles to look like water in motion, clicking "Shop Now" on the background image opens the shop page.
Added also a link to Video on Youtube with basic explanation about Set Up of Aquaponics System (video from 2014, old but chossed with for this poupose because the explanation of the set up and how it works is very good.)

### Shop page
Contains all the available products with different product categories(Hardware Basics, Seeds and Plants, and Fish Products).
Product can be sort by: Category, Price, Rating (base on owner opinion) and Name.

### Product Detail page
You can view the product detail, with description and rest of product info. 
Update quantity and "Add to cart" button available to add products to cart or continue shopping to go to all product page.

### Login / Register page / Logout
Login page with option to register if someone is not a member yet, login and  logout.

## Product Management
Admin and superuser allowed to add, edit or delete products.

### Profile page
If the user is logged in there is a Profile page, where the user can check their order history.

### Cart page
After a product is added to the cart, the user can view the containt of the cart here, update or delete products from the cart.
From here user can go to Checkout page to arrange card payment (Stripe), also login or sing up available from this page.

### Checkout page
User will see a Form to fill in all details for Payment with card and also Order History.
Options to go to payment or update cart in case user want to change/remove product or product quantity before complete order.

### Order confirmation
After payment user view a thank you page with order confirmation and delivery information. Automatically user receive an email with purchase history.
Or continue shopping button option.


## UX

### User stories:
* As a user I would like to be able to view the site on any device, including mobile, tablet, desktop.

* As a user I would like to be able to search to a keyword and sort products by price, name, category or rating in order to find what I need.

* As a user I would like to read more details about a product after clicking on it.

* As a user I would like to be able to find information about my previous orders.

* As a user I would like to be able to contact Aquaponics Shop with my questions.

* As a user I would like to be able to register on the site.

### Admin stories:
* As an admin I would like to be able to login to an administration panel to manage products or orders from users. Only allowed with superuser or shop owner.
* As an admin I don't want a user to be able to checkout an empty cart .
* As a admin I do not want a user can manage products.

## Design and colors
### Fonts
I used Noto Sans, from Google Fonts.
Sans-serif is used as the default backup font in case when Nunito Sans was not possible to load.

### Colors
#00A499 #09382C - Font colors.

#F2F4F5 #F2F4F5 - Background color, icons and , buttons shadow.

### Media
Background image from Unsplash.com and for some products image used as well. Rest of the images are from my own Aquaponics sytems or projects where I have participated. 

## Technology Used
Required: HTML, CSS, JavaScript, Python, Django, Postgres, Stripe payments ans AWS storage service.


### Languages:
* HTML5
* CSS3
* JavaScript
* Python 3.8

### Libraries, frameworks, tools used:
* Bootstrap 4 framework was used for developing a responsive, mobile-first website
* Django 3.1 as python web framework used for rapid development, maintainable, clean design
* jQuery JavaScript library to simplify HTML DOM manipulation
* Google Fonts Used Noto Sans fonts
* FontAwesome as icon provider
* Stripe made it possible to receive payments
* Psycopg2 as database adapter for the Python
* Gunicorn or Green Unicorn, a WSGI server implementation used to run Python web application
* VSCode was used as a code editor
* Git Version control
* Gitpot development enviroment
* Github used as a Git repository hosting service
* Heroku is a container-based cloud Platform, I used Heroku to deploy this app.
* Favicon Generator Used to make the right Favicon for the project, I converted the home page background image to a favicon.
* Unsplash Used to find the background images and some products pics.
* W3C Validator Used to check the validity of my HTML and CSS.
* PEP 8 Online Validator Used to check my Python code.
* Balsamic to create mockups.
* Compressjpg and CompresspngUsed to compress all my images.
* AWS S3 Bucket as a cloud storage
* Boto3 to make use of Amazon S3
* Pillow for saving image file formats
### Databases:
* PostgreSQL database service provided directly by Heroku
* SQlite3 provided by django


## Testing
During the development of the project I carried out testing, I used Google Chrome Developer Tools consistently to check each changes.
I have tested the site on Google Chrome, Safari and Firefox. And on the following mobile devices: Samsung S20 and on iPad tablet.

* Home page:
 Click on button **Shop Now**, goes to Product page, shows All Products, OK.
 Click on **Video**, goes to YouTube video, OK.


* Navigation:
Click on "logo": **Aquaponics Shop**, goes to home page. OK
Search by keyword, trying **search** "tray", goes to products including "Tray" on description or name. OK
Click on **My Account**, opens **My Profile**, **Logout**, **Register** and **Login**. All links work. OK
Click on **Cart**, opens products in Cart. If not products added to the cart, opens page to clik on "Kepp Shopping". OK
Click on **All Products** opens sear by: Price, Rating, Categotry. Click on each and all of them make a correct selection of products base on criteria. OK
Click on **Basics** opens different products: Growbeds&Pots, Plumbing, Electronics & Grow Lights, Grow Medium and All basics. Shows correct selection in all options. OK
Click on **Seeds & Plants** opens different products: Seeds, Baby Plants, All Seeds & Baby Plants. Shows correct selection in all options. OK
Click on **Fish Products** opens different products: Fish tanks, Fish Food, Aquarium accessories and All Fish Products. Shows correct selection in all options. OK
Number of products found visible in all categories, OK.
Click on **Sorting by**: Price (low to high), Price (high to low), Rating (low to high) or (high to low) , Name (A-Z) or (Z-A), Category (A-Z) or (Z-A). Working Ok.

* **All Products**, shows all products (24 found). OK Including: Image, description, price, rating and category.
* Click on any product, opens **Product detail** to view more details about the product and option to **Add product** to cart or update quantity. OK.
  Click on **Keep Shoping** goes to All products. OK
* Click on Cart opens **Shoping Cart** to view what we will buy, delivery cost included (10%) and if it is more than 60 Euros free. OK 
  Possible to remove product or update quantity. OK
  Click on Keep Shopping goes to All Products. OK
  Click on **Secure Checkout** goes to:
* **Checkout Form** mandatory to fill in all details, if not meessage info. OK
  Checkbox to save profile from order working OK. 
  Click on **Update Cart** goes back to Shopping Cart.
  Click on **Complete Order** goes to checkout_success page, with Order Confirmnation and email send to the user. OK
  Click on **Continue Shopping** goes to All Products. OK
  Payment tested using card numbers:
    No authentication (default U.S. card): 4242 4242 4242 4242.
    Authentication required: 4000 0027 6000 3184.
* **My Profile**, opens order/delivery history. OK
  Click on **Update information** to change profile records. OK
* Register, Login and Logout. Working with deficences, only signout/logout works properly. Register and Login not working.
* Email received with order confirmation and delivery info. OK
Pop up Alerts about different functions (suscess, info, error, alerts...) added and work properly. OK 

### Code Validation
CSS was validated using W3C CSS Validation Service.

HTML was validated using W3C Markup Validation Service.

Python code was validated using PEP8 online checker.

### Defensive design
Warning messages were used when user entered already taken username at registration, or wrong password/username when signing in.


## Deployment to Heroku

Steps to deploy to Heroku:
1.	Heroku .com click on New and Create new app.
2.	Named as: Aquaponics-shop. Region selected: Europe.
3.	In Resources tab , search and add Heroku Postgres. Select Hobby Dev (free)and click Provision.
4.	In Settings click on Reveal Config Vars, and copied the value of DATABASE_URL in Gitpot setting.
5.	Back to Gitpod in the Terminal install dj_data_base_url and psycopg2-bunary, typing: pip3 install psycopg2-binary and pip3 install dj_database_url.
6.	Created a requirements.txt file using the terminal command pip3 freeze > requirements.txt. Make sure Heroku installs all our apps requirements checking requirements.txt file.
7.	Go to settings.py and add import dj_database_url and update DATABASES = {'default': dj_database_url.parse(os.environ.get('DATABASE_URL'))} in the database settings.
8.	Env.py update, os.environ.setdefault("DATABASE_URL", "postgres://postgres key -  from Heroku").
9.	Migrate all changes to Postgres database typing: python3 manage.py makemigrations and then python3 manage.py migrate.
10.	In the Terminal, to load data categories use python3 manage.py loaddata categories.
11.	Create a super user: python3 manage.py createsuperuser.User name added, emaill and password.
12.	Install unicorn typing: pip3 install gnicorn in the Terminal to act as webserver and freeze that into our requirements file typing: pip3 freeze > requirements.txt.
13.	Create Procfile using command: echo web: gunicorn ms4.wsgi:application.
14. Git add ., git commit and git push.

To connect AWS: 
1.	Log in to Amazon AWS, went to S3 and created a new S3 bucket (aquaponics-shop)
2.	Returned to terminal window and run sudo pip3 install django-storages and sudo pip3 install boto3. Went to settings.py and added storages to INSTALLED_APPS.
3.	Also in settings.py the following lines are added:
        AWS_STORAGE_BUCKET_NAME = 'aquaponics-shop'
	    AWS_S3_REGION_NAME = 'eu-west-1'
	    AWS_ACCESS_KEY_ID = os.environ.get('AWS_ACCESS_KEY_ID')
	    AWS_SECRET_ACCESS_KEY = os.environ.get('AWS_SECRET_ACCESS_KEY')
	    AWS_S3_CUSTOM_DOMAIN = f'{AWS_STORAGE_BUCKET_NAME}.s3.amazonaws.com'
	
	    # Static and media files
        STATICFILES_STORAGE = 'custom_storages.StaticStorage'
	    STATICFILES_LOCATION = 'static'
	    DEFAULT_FILE_STORAGE = 'custom_storages.MediaStorage'
	    AWS_DEFAULT_ACL = None
	    MEDIAFILES_LOCATION = 'media'
	
	    # Override static and media URLs in production
	    STATIC_URL = f'https://{AWS_S3_CUSTOM_DOMAIN}/{STATICFILES_LOCATION}/'
	    MEDIA_URL = f'https://{AWS_S3_CUSTOM_DOMAIN}/{MEDIAFILES_LOCATION}/'
	
4.	Update env.py with AWS keys (these keys are from S3).
5.	Create custom_storages.py at the top level:
6.	Returned to terminal window and run python3 manage.py collectstatic
7.	Returned to Heroku. In Settings clicked on Reveal Config Vars button, and added all the following config vars from env.py:

![Heroku Config Var](/media/HerokuConfigVar.PNG)

8. Git push heroku master to finish and deploy to Heroku.
9. Clicked to Deploy tab, then GitHub, searched for my repository and clicked to Connect button.
Heroku will be updated automatically from Github repository.

## Credits 

### Acknowledgements
Big thanks to my mentor, Brian M and the Code Institute Slack channel, friends and family for help with testing and feedback.

### Disclaimer
*Educational Purposes Only*




