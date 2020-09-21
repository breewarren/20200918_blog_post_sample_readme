
# gravida.

A sample template of a README file, related to the [blog post](https://medium.com/swlh/creating-software-engineering-projects-a-structural-approach-3992637761e8) "Creating Software Engineering Projects — A Structural Approach" published by The Start Up on Medium's platform.<br/>
<br/>
Be sure to see the rest of my work on:
[Virtual Portfolio](https://www.sampleportfolio.com/) | [LinkedIn](https://www.linkedin.com/in/bree-warren/) |
[Github](https://github.com/breewarren) | 
[Medium](https://medium.com/swlh/creating-software-engineering-projects-a-structural-approach-3992637761e8)
# 
### Technical Description: 
A Command Line Interface App with CRUD functioning, incorporating:
* Object Relational Mapping (with ActiveRecord)
* SQL Databases (using sqlite3)
* Object Orientation Models (via Ruby)
* User-Friendly Navigation (with TTY prompts)

### App Description:
Gravida, a term rooted from Latin, refers to a pregnant woman. In medicine, this expresssion encompasses a measure of a patient's obstetric history. With our application, the User herself is able to also manage all of her pregnancies, along with the information of the corresponding medical provider (whether that is a physican, midwife, etc.), and as well as other informative features. 

-----
## Instructions
        In the terminal, run:
        - 'bundle install' to download neccesary gems
        - 'ruby app/run.rb' to begin the application
----

## Models & Relationships

### User | Pregnancy (Join Model) | MedicalProvider
<br />

### User <br />
* A User has many Pregnancies <br />
* A User has many MedicalProviders, through Pregnancies <br />

### Pregnancy <br />
* A Pregnancy belongs to a User <br />
* A Pregnancy belongs to an MedicalProvider <br />

### MedicalProvider <br />
* A MedicalProvider has many Pregnancies <br />
* A MedicalProvider has many Users, through Pregnancies <br />
----

## SQL Database Table Properties
### User Table Properties
* First Name
* Username
* Password
* Email Address
* Age

### Pregnancy Table Properties
* Description (ex: Name of Baby)
* Active Status (Ongoing or Concluded)
* Number of Weeks
* Due Date
* Date of Deliver/Loss
* Risk Level (Low or High)
* Life Status (Living, Stillbirth, Miscarriage, or Abortion)
* Delivery Type (Vaginal or Ceserean Section)
* Sex
* Quantity (if Twins, Triplets, etc.)
* User_ID (Foreign Key)
* MedicalProvider_ID (Foreign Key)

### MedicalProvider Table Properties
* Name
* Credentials
* Practice Name
* Years Experience
* Ratings (Star System)
* Subspecialty (Maternal Fetal, Infertility, etc.)

--------

## CRUD Functionality, aka User Stories
"." Designates class methods | "#" Designates instance methods

### Create
* User can create an account

        User#create_account
* User can create an instance of a pregnancy

        AppCLI.create_pregnancy
* User can create an instance of a MedicalProvider
        
        User#create_medical_provider
#
### Read
* User can view all account information 

        User#account_info
* User can view all pregnancies specific to oneself

        User#pregnancies
* User can view all MedicalProviders specific to oneself

        User#medical_providers
* User can view the pregnancies specific to the MedicalProvider

        MedicalProvider#pregnancies
* User can view information of a specific MedicalProvider

        MedicalProvider#obgyn_profile_info
#
### Update
* User can update account information

        User#update_account
* User can update an instance of one's own Pregnancy information

        User#update_pregnancy
* User can update an instance of one's own MedicalProvider information

        User#update_medical_provider
#
### Delete:
* User can deactivate one's own account

        User#deactivate_account
* User can delete an instance of a Pregnancy speficic to oneself

        User#delete_pregnancy
* User can delete an instance of a MedicalProvider specific to oneself

        User#delete_medical_provider
#
## Interface-Specific Methods:

    AppCLI.start
    AppCLI.welcome
    AppCLI.login
    AppCLI.homepage
    AppCLI.affirming_message
    AppCLI.comforting_message
    AppCLI.about_gravida
    AppCLI.exit
#
## Additional Methods, aka Stretch Goals:

* User can be provided gravida/para/abortus score, along with explanation

* User can view total number of pregnancies associated with account

* User can view the first or last pregnancy entry


* User can be provided trimester information of a pregnancy

* User can search an instance of a pregnancy, by its name/description

* User can be provided term length (pre- or full-term)

* User can view the MedicalProvdier with the highest review

* User can view MedicalProviders with the most experience

* User can view Medical Providers with the most successful deliveries


-----

### Video Demo:
 [Video Demo Link](https://video.com/blahblahblah)


## Thank you! <br> Bree Warren