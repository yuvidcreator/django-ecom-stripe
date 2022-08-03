# Django_Project_Ecommerce

## Instructions

1. Download
2. Extract in a folder
3. Open with visual studio code

Commands:

    py -m venv venv
    venv\Scripts\activate
    pip install -r requirements.txt
    py manage.py runserver


In core /settings.py the stripe is commented out - just put your own details in here (not all of these are connected to the project)

# Stripe Payment
PUBLISHABLE_KEY = ''
SECRET_KEY = ''
STRIPE_ENDPOINT_SECRETE = 'whsec_bcc34f2a275f651e3b23a695226f0d94993893324c29cbc8d6153635d9ccc8cb'
# by runing 
# You will get output in server terminal ---> copy 'webhook signing secret' and paste it in STRIPE_ENDPOINT_SECRETE=''
# Ready! You are using Stripe API Version [2020-08-27]. Your webhook signing secret is whsec_bcc34f2a275f651e3b23a695226f0d94993893324c29cbc8d6153635d9ccc8cb (^C to quit)

# To use stripe cli - https://stripe.com/docs/stripe-cli/about-events
# Download from - https://github.com/stripe/stripe-cli/releases/tag/v1.10.3
# To get STRIPE_ENDPOINT_SECRETE, run below command on serverside stripe cli
on windows 10 --> stripe listen --forward-to localhost:8000/payment/webhook/
on linux --> sudo ./stripe listen --forward-to localhost:8000/payment/webhook/

# Admin login
1. http://127.0.0.1:8000/admin
2. username and password = admin