# Host-Checker
This is a simple program that takes the input of the target host and uses Nmap, GoBuster, and WhatWeb to scan the target host.

## Description

This is a simple program that takes the input of the target host and uses Nmap, GoBuster, and WhatWeb to scan the target host. The program is a static command line program that shows the user in a visual fashion what ports are open, the directories of the server, and the WhatWeb report (WHOIS) of the host.

## Getting Started

### Dependencies

* NO DEPENDENCIES REQUIRED!!!

### Installing

* No real install needed, just make sure you have the bash terminal updated
```
sudo apt update
sudo apt upgrade
```

### Executing program

* Run the program like any other common bash script.
```
bash recon.sh <IP>
```

### Example Run
```
~# ./recon.sh 10.10.0.50

Running Nmap...
Running Gobuster...
Running WhatWeb...
/usr/lib/ruby/vendor_ruby/target.rb:188: warning: URI.escape is obsolete

----- NMAP -----

PORT     STATE SERVICE
21/tcp   open  ftp
22/tcp   open  ssh
23/tcp   open  telnet
25/tcp   open  smtp
53/tcp   open  domain
80/tcp   open  http
111/tcp  open  rpcbind
139/tcp  open  netbios-ssn
445/tcp  open  microsoft-ds
512/tcp  open  exec
513/tcp  open  login
514/tcp  open  shell
1099/tcp open  rmiregistry
1524/tcp open  ingreslock
2049/tcp open  nfs
2121/tcp open  ccproxy-ftp
3306/tcp open  mysql
5432/tcp open  postgresql
5900/tcp open  vnc
6000/tcp open  X11
6667/tcp open  irc
8009/tcp open  ajp13
8180/tcp open  unknown

----- DIRS -----

/.hta (Status: 403)
/.htaccess (Status: 403)
/.htpasswd (Status: 403)
/.bash_history (Status: 200)
/cgi-bin/ (Status: 403)
/dav (Status: 301)
/phpMyAdmin (Status: 301)
/index (Status: 200)
/index.php (Status: 200)
/test (Status: 301)
/twiki (Status: 301)
/phpinfo (Status: 200)
/phpinfo.php (Status: 200)

----- WEB -----

WhatWeb report for http://10.10.0.50
Status    : 200 OK
Title     : Metasploitable2 - Linux
IP        : 10.10.0.50
Country   : RESERVED, ZZ

Summary   : WebDAV[2], X-Powered-By[PHP/5.2.4-2ubuntu5.24], Apache[2.2.8], PHP[5.2.4-2ubuntu5.24], HTTPServer[Ubuntu Linux][Apache/2.2.8 (Ubuntu) DAV/2]

Detected Plugins:
[ Apache ]
        The Apache HTTP Server Project is an effort to develop and
        maintain an open-source HTTP server for modern operating
        systems including UNIX and Windows NT. The goal of this
        project is to provide a secure, efficient and extensible
        server that provides HTTP services in sync with the current
        HTTP standards.

        Version      : 2.2.8 (from HTTP Server Header)
        Google Dorks: (3)
        Website     : http://httpd.apache.org/

[ HTTPServer ]
        HTTP server header string. This plugin also attempts to
        identify the operating system from the server header.

        OS           : Ubuntu Linux
        String       : Apache/2.2.8 (Ubuntu) DAV/2 (from server string)

[ PHP ]
        PHP is a widely-used general-purpose scripting language
        that is especially suited for Web development and can be
        embedded into HTML. This plugin identifies PHP errors,
        modules and versions and extracts the local file path and
        username if present.

        Version      : 5.2.4-2ubuntu5.24
        Google Dorks: (2)
        Website     : http://www.php.net/

[ WebDAV ]
        Web-based Distributed Authoring and Versioning (WebDAV) is
        a set of methods based on the Hypertext Transfer Protocol
        (HTTP) that facilitates collaboration between users in
        editing and managing documents and files stored on World
        Wide Web servers. - More Info:
        http://en.wikipedia.org/wiki/WebDAV

        Version      : 2

[ X-Powered-By ]
        X-Powered-By HTTP header

        String       : PHP/5.2.4-2ubuntu5.24 (from x-powered-by string)

HTTP Headers:
        HTTP/1.1 200 OK
        Date: Wed, 19 Jun 2019 18:03:39 GMT
        Server: Apache/2.2.8 (Ubuntu) DAV/2
        X-Powered-By: PHP/5.2.4-2ubuntu5.24
        Connection: close
        Transfer-Encoding: chunked
        Content-Type: text/html
```

## Help
Common problems or issues are that you are not using an authorized user and need to switch to root.
```
sudo bash recon.sh <IP>
```

## Authors

Contributors names and contact info

Christopher Hyatt (me)
* [@codeslacker1155](https://github.com/codeslacker1155)

## Version History

* 0.2
    * Various bug fixes and optimizations
    * See [commit change]() or See [release history]()
* 0.1
    * Initial Release

## License

This project is licensed under the [GNU Privacy v3] License - see the LICENSE.md file for details

## Acknowledgments

Inspiration taken from a list of basic programs to make in any language that I have in a random text file of ideas.
