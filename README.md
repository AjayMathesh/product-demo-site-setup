# DEMO SITE SETUP PROCESS
====================================================================
# cPanel setup:
1. Login to cPanel with Credentials
2. Go to file manager -> public_html
4. Go to mysql databases menu under databases section
5. Create new database by typing new name and create it.
6. Scroll down and create a database user 
7. Assign a created user to the created database.
8. set user privileges by giving all privileges
9. Download Wordpress from wordpress.org
10. Paste and extract the WordPress zip file in the respected folder (which points your demosite domain url)
11. Setup and install the wordpress site by accessing the endpoint of the domain in cPanel
12. Give the Database credentials(Database name and password) which you have created through cPanel (Step 3,4).

# To activate multisite in WordPress:
1. Open the `wp-config.php` file from the WordPress folder.
2. Add this line above where it says `/* That's all, stop editing! Happy publishing. */`:

    ```php
    define( 'WP_ALLOW_MULTISITE', true );
    ```

3. After that, go to the WordPress admin dashboard -> Tools -> Network setup and click Install.
4. After clicking Install, it will display two code blocks which need to be pasted in `wp-config.php` and `.htaccess` files respectively.
5. Paste those codes carefully by reading the instructions.
6. After all this process you can see the My sites Menu on the top left of the admin dashbaord, where you can manage your multisite network.
   For Eg:-
   https://i0.wp.com/wordpress.org/support/files/2018/11/network-admin-link.png?fit=383%2C184&ssl=1
7. To create new sub-site go to My Sites->Network Admin-> Add New site

# Plugin installations and customization process
1. Go to My sites-> Network admin-> Plugins
2. Install the plugins such as multisite-cloner, flycart-demo-promotion, create-demo sub site, disable emails
3. The demo-site should be handled by 2 sites. One is a main site and another one is a subsite (If you have only main site create sub site by going to My Sites->Network Admin-> Add New site).
4. Go to Appearance -> Theme -> and install Storefront theme and storefront child theme.
5. Activate store front child theme in the main site and storefront theme in sub site.
6. Go to the ``wp-content`` folder and edit a file ```storefront-child-theme/header.php``` with the below content to design a header.
7. After that install a AAM plugin in network
``https://wordpress.org/plugins/advanced-access-manager/``
The AAM plugin will help us to manage user roles and user specific access


