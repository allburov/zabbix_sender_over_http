<?php
function get_client_ip() {
    $ipaddress = '';
    if (getenv('HTTP_CLIENT_IP'))
        $ipaddress = getenv('HTTP_CLIENT_IP');
    else if(getenv('HTTP_X_FORWARDED_FOR'))
        $ipaddress = getenv('HTTP_X_FORWARDED_FOR');
    else if(getenv('HTTP_X_FORWARDED'))
        $ipaddress = getenv('HTTP_X_FORWARDED');
    else if(getenv('HTTP_FORWARDED_FOR'))
        $ipaddress = getenv('HTTP_FORWARDED_FOR');
    else if(getenv('HTTP_FORWARDED'))
       $ipaddress = getenv('HTTP_FORWARDED');
    else if(getenv('REMOTE_ADDR'))
        $ipaddress = getenv('REMOTE_ADDR');
    else
        $ipaddress = 'UNKNOWN';
    return $ipaddress;
}


//header("Content-type: text/xml; charset=windows-1251");
$server=$_GET['server'];
$key=$_GET['key'];
$value=$_GET['value'];
$zabbix_server_address="devops-zabbix.ptsecurity.com";
$path_to_log_file="/var/log/zabbix_sender/zabbix_sender.log";

if (empty($server)){
        echo "parametr SERVER is EMPTY";
        $ip_address=get_client_ip();
        $error_msg= date('Y-m-d H:i:s') . " - ZABBIX_SENDER[warning] - FROM: $ip_address; HTTP_PARAM: server=$server, key=$key, value=$value; ERROR: parametr SERVER is EMPTY\n";
        error_log($error_msg,3,$path_to_log_file);
        exit;
}

if (empty($key)){
        echo "parametr KEY is EMPTY";
        $ip_address=get_client_ip();
        $error_msg= date('Y-m-d H:i:s') . " - ZABBIX_SENDER[warning] - FROM: $ip_address; HTTP_PARAM: server=$server, key=$key, value=$value; ERROR: parametr KEY is EMPTY\n";
        error_log($error_msg,3,$path_to_log_file);
        exit;
}

if ($value==""){
        echo "parametr value is EMPTY";
        $ip_address=get_client_ip();
        $error_msg= date('Y-m-d H:i:s') . " - ZABBIX_SENDER[warning] - FROM: $ip_address; HTTP_PARAM: server=$server, key=$key, value=$value; ERROR: parametr VALUE is EMPTY\n";
        error_log($error_msg,3,$path_to_log_file);
        exit;
}

$exec_str="/usr/bin/zabbix_sender -z $zabbix_server_address -p 10051 -s ".escapeshellarg($server)." -k ". escapeshellarg($key)." -o ". escapeshellarg($value);
exec($exec_str,$out, $err);
if ($err==0){
        echo "OK";
}
else {
        //print to html
        echo "ERROR:";
        echo "</br>";
        echo "server=$server, key=$key, value=$value";
        echo "</br>";
        var_dump($out);
        echo "</br>";
        var_dump($err);

        //Log error
        $ip_address=get_client_ip();
        $error_msg= date('Y-m-d H:i:s') . " - ZABBIX_SENDER[error] - FROM: $ip_address; HTTP_PARAM: server=$server, key=$key, value=$value; ERROR: zabbix_sender: $out[0]\n";
        error_log($error_msg,3,$path_to_log_file);

}
