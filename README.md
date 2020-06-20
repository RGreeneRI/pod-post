# Pod Post - A Wordpress Plugin

A modified version of [Paul Sheldrake's](http://www.fractured-state.com/2011/09/mp3-to-post-plugin/) mp3-to-post [plugin](https://wordpress.org/plugins/mp3-to-post/) to get it to work with Wordpress 5.4.1, and PHP 7.1.24.  This plugin creates  posts from MP3 ID3 information and attaches the MP3 file to the post.

- Contributors: Rich Greene
- Tags: mp3, podcasting, id3, podcast, podcaster, audio, music, spokenword
- Requires at least: Unknown
- Tested up to: 5.4.2
- Stable tag: 0.9
- License: GPLv3


# Description

This plugin creates a folder that you can STFP or SSH MP3 files in to and then 
scans the folder to create the posts from the MP3 ID3 information.  

The ID3 tags are mapped to the posts data as follows:
ID3 Title -> Post Title
ID3 Comment -> Post Content
ID3 Genre -> Post Category



# Installation

1. Upload the plugin directory to the `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Upload mp3 files to /wp-content/uploads/pod-post
4. Go to the plugin page(on the admin side bar) and start creating posts.


# Frequently Asked Questions

= How can I look at/edit ID3 information =

You can use iTunes to edit ID3 information.   If you right click on the MP3 file there should be an option for 'Get Info' in the menu.   Clicking that open a dialogue where you can set the information.   Something to note is that setting the information in iTunes doesn't always set the ID3v1 and ID3v2 tags, it often just sets the v1 tags.  

If you go to download.com and search for 'ID3 Editor' you will find a variety of free options if iTunes isn't working for you.

In Windows you can also right click the mp3 file and select Properties.  In the Summary tab there is an option to enter ID3 information.


# Changes from MP3 to Post
- Modified to get it working on Wordpress 5.4.2 and PHP 7.1.32
- Updated to use id3v2 thats built into wordpress
- Added button to delete mp3 files < 512k (in pod-post upload dir)
- Added button to delete ALL mp3 files (in pod-post upload dir)
- Added button to create 5 posts per click, in addition to the original All or 1
- Removed instructions from admin page for cleaner look
- Hardwired to set posts to publish (rather than draft or checkbox to publish)
- Added `[audio]` shortcode to posts to embed player


# PS
I'm doing this as a hobby, and learning PHP through trial and error.  If you're smart and see something that needs fixing, please let me know.  Thanks!


# Help
I changed the old like_escape to wpdb::esc_like, but I'm getting the following error (while in debuggung mode):

Deprecated:  "Non-static method wpdb::esc_like() should not be called statically in .../wp-content/plugins/pod-post/pod-post.php on line 147".  It still works anyways though...
