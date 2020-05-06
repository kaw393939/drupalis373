Prerequisttes

1.  Install git if you haven't
2.  Install Docker Desktop if you haven't

Commands:

1.  git clone this repo:

2.  Go to the folder that you git clone to i.e. it will be a sub directory of whatever folder you ran the command in

3.  Run:  docker-compose up -d to start the download process of drupal and what it needs to run.  It will take a while the first time because you have to download a lot of stuff maybe 300-500mb

4.  Once this is done, go to http://localhost:8080

5.  Click save and continue

6.  Click Save and continue, you don't need to select anything

7.  Click advanded and enter all of the following for connecting to the database:

select postgres as database with the following parameters: dbname=postgres user=postgres pass=example hostname=postgres

advanced is where you enter in the hostname "postgres" as seen above

8.  click save and continue and watch it install

9.  enter in the account information you will use to login to the site. Quick tip... make the username and password admin / admin so you don't forget and need to start all over again

10.  You should see the drupal site after you save this and continue

Docker commands from the directory you are in:

1.  To destory the site AND START ALL OVER type: docker-compose down
2.  To start the site type docker-compose up
3.  To stop the site and not destroy it type: docker-compose stop

Notes:

1.  Click on structure -> block layout  to position content blocks.  You can control where blocks appear on the site by editing them and putting a path for the block invisability settings.  There instructions throughout drupals menu to tell you how to do things like this when you look below the fields in forms.

2.  Click structure menus to create menus and edit them.  Each time you add a menu you can go to the blocks screen to place it in the site as described above by clicking the add button next to the region you want to put the block / menu block

3.  click on content and the add content button to add either a page or article

4.  you can add different types of content like events by going to structure -> content types and creating a content type. 

5.  you can add views that are pages with that query the database for content by going to structure -> views and clicking create view there are a lot of options but some are obvious what they should do and they give you a basic template when you create the view that you can set options for to place it in a menu

6.  There are drupal themes and modules.  You can usually just google something like add drupal date field or add drupal calendar and they will tell you what module to put in.  Zyou just click appearance to add themes by putting the url to the theme you find on drupal.org and you do the same for modules but you click on extend

I hope these tips help and just click around, you can easily create or destory sites.  IF you want more sites you will need to copy this folder and change the port that the servers start up on for apache and postgres, if you want to run more than one site at the same time.  You don't need to do this if you just stop the current site and do a docker compose on a new site from within a different folder.


