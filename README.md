# Pod Post
A modified version of [Paul Sheldrake's](http://www.fractured-state.com/2011/09/mp3-to-post-plugin/) mp3-to-post [plugin](https://wordpress.org/plugins/mp3-to-post/) to get it to work with Wordpress 5.4.1, and PHP 7.1.24.  This plugin creates wordpress posts from MP3 ID3 information and attaches the MP3 file to the post.

# Changes
- Modified to get it working on Wordpress 5.4.2 and PHP 7.1.32
- Updated to use id3v2 thats built into wordpress
- Added button to delete mp3 files < 512k (in mp3-to-post upload dir)
- Added button to delete ALL mp3 files (in mp3-to-post upload dir)
- Added button to create 5 posts per click, in addition to the original All or 1
- Removed instructions from admin page for cleaner look
- Hardwired to set posts to publish (rather than draft or checkbox to publish)
- Added `[audio]` shortcode to posts to embed player

# PS
I'm doing this as a hobby, and learning PHP through trial and error.  If you're smart and see something that needs fixing, please let me know.  Thanks!

# Help
I changed the old like_escape to wpdb::esc_like, but I'm getting the following error (while in debuggung mode):

Deprecated:  "Non-static method wpdb::esc_like() should not be called statically in .../wp-content/plugins/mp3-to-post/mp3-to-post.php on line 147".  It still works anyways though...
