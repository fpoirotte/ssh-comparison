---
title: pssht
homepage: https://github.com/fpoirotte/pssht
source-repository: https://github.com/fpoirotte/pssht
license: "[MIT](https://github.com/fpoirotte/pssht/blob/master/LICENSE)"
first-release:
    date: 2014-12-30
latest-release:
    version: 0.1.1
    date: 2015-05-08
changelog: "https://github.com/fpoirotte/pssht#changelog"
client: no
server: yes
library: yes

protocols:
    cipher:
        - 3des-cbc
        - 3des-ctr
        - aes128-cbc
        - aes128-ctr
        - aes128-gcm@openssh.com
        - aes192-cbc
        - aes192-ctr
        - aes256-cbc
        - aes256-ctr
        - aes256-gcm@openssh.com
        - arcfour
        - arcfour256
        - arcfour128
        - blowfish-cbc
        - blowfish-ctr
        - cast128-cbc
        - cast128-ctr
        - chacha20-poly1305@openssh.com
        - idea-cbc
        - idea-ctr
        - none
        - rijndael-cbc@lysator.liu.se
        - serpent128-cbc
        - serpent192-cbc
        - serpent256-cbc
        - serpent128-ctr
        - serpent192-ctr
        - serpent256-ctr
        - twofish-cbc
        - twofish128-cbc
        - twofish192-cbc
        - twofish256-cbc
        - twofish128-ctr
        - twofish192-ctr
        - twofish256-ctr
    compression:
        - none
        - zlib@openssh.com
        - zlib
    hostkey:
        - ecdsa-sha2-nistp256
        - ecdsa-sha2-nistp384
        - ecdsa-sha2-nistp521
        - ssh-dss
        - ssh-ed25519
        - ssh-rsa
    kex:
        - curve25519-sha256@libssh.org
        - ecdh-sha2-nistp256
        - ecdh-sha2-nistp384
        - ecdh-sha2-nistp521
        - diffie-hellman-group14-sha1
        - diffie-hellman-group1-sha1
    mac:
        - hmac-md5
        - hmac-md5-etm@openssh.com
        - hmac-md5-96
        - hmac-md5-96-etm@openssh.com
        - hmac-ripemd160
        - hmac-ripemd160@openssh.com
        - hmac-ripemd160-etm@openssh.com
        - hmac-sha1
        - hmac-sha1-etm@openssh.com
        - hmac-sha1-96
        - hmac-sha1-96-etm@openssh.com
        - hmac-sha2-256
        - hmac-sha2-256-etm@openssh.com
        - hmac-sha2-512
        - hmac-sha2-512-etm@openssh.com
        - none
        - ripemd160
        - umac-64@openssh.com
        - umac-64-etm@openssh.com
        - umac-128@openssh.com
        - umac-128-etm@openssh.com
    userauth:
        - publickey
        - password
        - hostbased
        - none
    extension:
        - delay-compression

first_kex_packet_follows: 0
ident: "SSH-2.0-pssht_1.0.x_dev"
---
* PHP implementation of an SSHv2 server for educationnal purposes
* Provides only basic operations (no SFTP/SCP, no shell spawning, no SSH agent/X11/port forwarding)
* Mostly useful as a library to embed a custom SSH server inside an application
* The [example application](https://github.com/fpoirotte/pssht/blob/master/src/Application/EchoService.php) acts as a simple echo server
