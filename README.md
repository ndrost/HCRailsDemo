HCRailsDemo
===========

Just a rails CRUD app to demo heroku connect.

Setup
=====

Get a SE Demo Force app.

Install this app onto Heroku, install a Postgres DB, and install Heroku Connect.

Map the following fields over in Heroku Connect:

 * billingstate 
 * billingpostalcode
 * billingcountry
 * billinglatitude
 * billingcity       
 * billingstreet    
 * name              

After your first sync, your postgres table should look like this (use `\d salesforce.account` in `heroku pg:psql` to view it)

                                                Table "salesforce.account"
          Column       |            Type             |                            Modifiers                            
    -------------------+-----------------------------+-----------------------------------------------------------------
     billingstate      | character varying(80)       | 
     fax               | character varying(40)       | 
     billinglatitude   | double precision            | 
     billingcity       | character varying(40)       | 
     id                | integer                     | not null default nextval('salesforce.account_id_seq'::regclass)
     billingcountry    | character varying(80)       | 
     _c5_source        | character varying(18)       | 
     name              | character varying(255)      | 
     billingpostalcode | character varying(20)       | 
     billingstreet     | character varying(255)      | 
     billinglongitude  | double precision            | 
     lastmodifieddate  | timestamp without time zone | 
     recordtypeid      | character varying(18)       | 

Launch the app

