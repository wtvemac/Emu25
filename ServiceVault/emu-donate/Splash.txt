$SonTVRev="SonicServices Alpha v1.0 Rev 31";


$tosendout=<<"ERIC"
<html> 
<head> 
<display nooptions nostatus skipback clearback fontsize=medium showwhencomplete> 
<title>SonTV</title> 
</head> 
<body bgcolor="#000000" text="#449944" vlink="#449944" link="#449944" onLoad="GoHome()"> 
<script>
function GoHome() {
setTimeOut("location.href=('sontv:/home')",5000);
}
</script>
<bgsound src="file://ROM/Sounds/Splash.mid">
<center> 
<spacer type=block height=128 width=21> 
<img src="file://ROM/Images/MicrosoftName.gif"><img src="file://ROM/Images/MicrosoftR.gif"><br> 
<img src="file://ROM/Images/SplashLogo1.gif"> 
<br><br> 
<p><br> 
<p><br> 
<table border> 
<tr><td width=150> 
<a href="sontv:/home" selected nohighlight>SonTV</a> 
<tr><td> 
$SonTVRev</table> 
</center> 
</body> 
</html>
ERIC
    ;

undef $SonTVRev;

print $clients "200 OK\n"; 
print $clients "Connection: Keep-Alive\n"; 
print $clients "wtv-noback-all: wtv-\n"; 
print $clients "wtv-expire-all: wtv-\n";
print $clients "wtv-noback-all: sonictv\n"; 
print $clients "wtv-expire-all: sonictv\n"; 
print $clients "wtv-service: reset\n"; 
print $clients "wtv-service: name=wtv-mail host=209.240.199.119 port=1608 flags=0x04\n"; 
print $clients "wtv-service: name=mailto host=209.240.199.119 port=1608 flags=0x04\n"; 
print $clients "wtv-service: name=wtv-1800 host=$sockhost port=$sockport flags=0x04 connections=3\n"; 
print $clients "wtv-service: name=http host=209.240.194.41 port=1650 flags=0x04\n"; 
print $clients "wtv-service: name=ftp host=209.240.194.41 port=1650 flags=0x04\n"; 
print $clients "wtv-service: name=file host=209.240.194.41 port=1650 flags=0x04\n"; 
print $clients "wtv-service: name=gopher host=209.240.194.41 port=1650 flags=0x04\n"; 
print $clients "wtv-service: name=news host=209.240.198.116 port=1605 flags=0x04\n"; 
print $clients "wtv-service: name=wtv-news host=209.240.198.116 port=1605 flags=0x04\n"; 
print $clients "wtv-service: name=wtv-forum host=209.240.198.116 port=1605 flags=0x04\n"; 
print $clients "wtv-service: name=wtvchat host=209.240.199.78 port=1630 flags=0x04\n"; 
print $clients "wtv-service: name=wtv-chat host=209.240.198.116 port=1630\n"; 
print $clients "wtv-service: name=wtv-tricks host=$sockhost port=$sockport flags=0x04 connections=3\n";
print $clients "wtv-service: name=sontv host=$sockhost port=$sockport flags=0x04 connections=3\n"; 
print $clients "wtv-service: name=wtv-box host=$sockhost port=$sockport flags=0x04 connections=3\n"; 
print $clients "wtv-service: name=wtv-setup host=$sockhost port=$sockport flags=0x04 connections=3\n"; 
print $clients "wtv-service: name=wtv-log host=$sockhost port=$sockport flags=0x04\n";
print $clients "wtv-service: name=wtv-video host=$sockhost port=$sockport flags=0x04\n"; 
print $clients "wtv-service: name=wtv-help host=$sockhost port=$sockport flags=0x04\n"; 
print $clients "wtv-service: name=wtv-star host=$sockhost port=$sockport flags=0x04\n"; 
print $clients "wtv-service: name=wtv-build host=$sockhost port=$sockport flags=0x04\n"; 
print $clients "wtv-service: name=wtv-debug host=$sockhost port=$sockport flags=0x04 connections=3\n"; 
print $clients "wtv-service: name=wtv-help host=$sockhost port=$sockport flags=0x04\n"; 
print $clients "wtv-service: name=wtv-SrvTrigger host=$sockhost port=$sockport flags=0x04\n"; 
print $clients "wtv-user-name: Son$userssid\n"; 
print $clients "wtv-human-name: SonTV User\n"; 
print $clients "wtv-input-timeout: 1500\n"; 
print $clients "wtv-inactive-timeout: 0\n"; 
print $clients "wtv-connection-timeout: 120\n"; 
print $clients "wtv-fader-timeout: 900\n"; 
print $clients "wtv-relogin-url:  sontv:/home\n"; 
print $clients "wtv-reconnect-url: sontv:/home\n"; 
print $clients "wtv-favorite-url: sontv:/home\n"; 
print $clients "wtv-favorite-index-url: sontv:/home\n"; 
print $clients "wtv-log-url: wtv-log:/log\n"; 
print $clients "wtv-show-time-enabled: true\n"; 
print $clients "wtv-name-server: 209.240.198.142\n";
print $clients "wtv-name-server: 209.240.198.141\n";
print $clients "wtv-irc-nick: Son$userssid\n";
print $clients "wtv-mail-url: http://www.transload.net/tl2/\n"; 
print $clients "wtv-notifications-url: sontv:/home\n"; 
print $clients "wtv-ssl-log-url: wtv-log:/log\n"; 
print $clients "wtv-favorites-folders-url: sontv:/home\n"; 
print $clients "wtv-ssl-timeout: 240\n"; 
print $clients "wtv-login-timeout: 7200\n"; 
print $clients "wtv-search-url: http://www.metacrawler.com/\n"; 
print $clients "wtv-bypass-proxy: true\n";
print $clients "wtv-allow-dsc: true\n";
print $clients "wtv-encryption: false\n"; 
print $clients "wtv-explore-url: sontv:/gotoSonicProductions\n"; 
print $clients "wtv-ticket: 1i2G9EYsDHjoGzsX17zztxScr4e9Z5WseZLwwgsU8io7ETT6gf9YTsXcUA1x+m7qzviXhGEUUZ/sWZOzF4F9npnDR3AuWgOcWxXDMbhQe8iMhzUln/q9O+38jvxBrZiUDr1248BiIxd1nJlEuduSYNTLMyYJ0lPsxHZekqGlHFL92JxKDk4eusPKON5gjCStc/K+e0afz/wtuS4e3lZnOyJmx5SaLXpCXm5wuvwvBdJAfflexhYDmehYhwq5oze8CV5cONEhV5RRtDDT7ucFI/86UJ3PBF40zTCR2yN+d/hk7fDOXxV0jm+UYlN/0vuc+dVBMgVgwL1YZ3eXlIM+gYKTwWgR6enngfP/uIW91721QlgmVo52WdbIaHViFYfIMIoQ0JtvyMS9f9S7kUMuCSoWsNg+HxScrbGLDTewXLi9Kt4QxXsC7IGpmuZRtR4nV4GRGzfaft2vuw/ql92iB0sae7VRVwqSRODPoVjcKFxxb8R0331YDfnNPnhqs0Zn0iptxCxDrfuS76jg8XYAD4pz0uQG6hGCcG2I8+ECwoqjR4IHBfmNaUyrXOw6p0Ekr9jqUHT5YHneYDI0eIhlRpZicQ1LJTXbc6kXRWAz55OnXfEjPs7bfI+hN1ARW6dHDzPrfC7HpCx+KfxSsjNRdxG6DAHVDiuh6LrzgzrnQwR18II4/XvoZwdmnOrHUxo4HOxAZLSO68irWJsmVSD1avhSl9bf3cDPZHHtD8NOEXnnx0YTnis24ZCOJjcHpWPbpsNItuSGE52xgJuuyyllmL1WJcmj6EosOObVZCzfw986H8N29wwapjHIdAmVx7X87Kxzt33DzDtXSBIwShdfZQ10zkZNN9G7pKUTHhzJQz3JCIAtCgua6IUa9JtUvnYzu6D7LFl0qOHITz6yjLy3vV8dv0xQ7qphOwEKSATqZXbx/1eVLX1ylgLq4ZAb0Hkte58xSz3jhStHOhRwd3is0o7JadTIyJuc5H1OsDQNuRVBr6Cikf8RvIzkcQzhUyD2N3CPUkeeQwDZOiXr8k01GMDLYV56UEg0cbzCkTMrwpb90cc9OglyCEdjaVXVebwS/Qmwq+m42QWtnHGQUHn2z9LAMDl/cQQ8MWwet4xXRn1hPssYUU+FdV6zv5/ejtfPrhV4463GKJpIUo5L+L81jRqISEIcf8fXPn13xBkueQTLhZblYy7ucl2hJ4O7mB+lH+AaiJzkZYBEBGALljAoUSdF1sB+TdMtwVLjp23XFpoQmVOZz0AgZ4dxHTlvy81ZOkb122MgTHFGMterKBqbI+jhpby0zQb77UUs/hxLCvXmDgBaa6uVmNNL0VcjveGLKyxRlYAnOVYZ2/7WloMLaMHQbA+zD4qeuEK0Up3G+B9KMK8SghIEyeB66yAsXL36zQAaYuXFedwH04fIS5QoluBTdaNDyNmaLcNJjcLebV6gU2aZ7+oSNFGfHisv1s3jDyrEnr1oLxadhhE/qf84lWKDXg790qMkHcbfGIbkS5BbB1WxsNkEW/LaHwyqMsGniEmD+si8Bi9kEnGLd/wnGgqKkymf6COtJ7EVzlSCfRleaA7IJ3ffYfuCk37n2TNZtNzLVWR13thE94hKrMBLKO+9lMcYgNevNI9TF89yZIqL6sZEZi+KEmA2/+UBX60GOd8UOg4+OoooNmmb+8uPY59NaN9+P/qyf9KFWRmI7XVNu+5NWuyNujW1ENDjhVhf9/nM++LBF5nXXW1NuG3+NR8tz73TP6ieY7NhyvMLHK9NF/HcpMqf6OikcO9hoP75\n";
print $clients "wtv-home-url: sontv:/home\n"; 
print $clients "wtv-settings-url: sontv:/setup\n";
print $clients "Content-length: ".length($tosendout)."\n"; 
print $clients "Content-type: text/html\n\n"; 
print $clients $tosendout;

$SonTVLogin=1;