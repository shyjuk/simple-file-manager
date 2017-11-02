simple-file-manager
===================

## Screenshot

![Screenshot](https://raw.github.com/jcampbell1/simple-file-manager/master/screenshot.png "Screenshot")

A Simple PHP file manager.  The code is a single php file.  

Just copy `index.php` to a folder on your webserver.  

## Why it is good

- Single file, there are no images, or css folders.  
- Ajax based so it is fast, but doesn't break the back button
- Allows drag and drop file uploads if the folder is writable by the webserver (`chmod 777 your/folder`)
- Suits my aesthetics.  More like Dropbox, and less like Windows Explorer
- Works with Unicode file names
- The interface is usable from an iPad
- XSRF protection, and an optional password.

## Do not allow uploads on the public web

If you allow uploads on the public web, it is only a matter of time before your server is hosting and serving very illegal content. Any of the following options will prevent this:
 - Don't make the folder writable by the webserver `chmod 775`
 - Set `$allow_upload = false`
 - Use a password `$PASSWORD = 'some password'`
 - Use a `.htaccess` file with Apache, or `auth_basic` for nginx
 - Only use this on a private network

## Troubleshooting

If you can not find the upload function check the folder permission.

- chown -R www-data:www-data simple-file-manager direcory

HT: [@beardog108](https://github.com/beardog108)
