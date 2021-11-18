Info | RPM | DPKG
---- | ----| ----
Check signature | rpm --checksig pckg | ??? debsig-verify
Install pckg | rpm -ivh pckg | dpkg -i
Check dependacies | rpm -qpR pckg | dpkg-deb --info pckg
Install pckg without dependacies | rpm -ivh --nodeps pckg | dpkg --force-depends -i pckg
Check installed pckg | rpm -q pckg | dpkg-query -l pckg
List all files of an installed pckg | rpm -ql pckg | dpkg-query -L pckg
List recently installed pckg | rpm -qa --last | ????
List all installed pckg | rpm -qa | dpkg-query -W -f=???
Upgrade pckg | rpm -Uvh pckg | dpkg -i pckg
Remove pckg | rpm -evv pckg | dpkg -r pckg
Remove pckg without dependencies | rpm -ev --nodeps pckg | dpkg -r --force-depends pckg
Query a file that belongs which Package | rpm -qf file | dpkg-query --search file
Query a Information of Installed Package | rpm -qi pckg | dpkg-query -p pckg
Get the Information of Package Before Installing |rpm -qip pckg | dpkg-deb -W pckg
How to Query documentation of Installed Package | rpm -qdf pckg | ???
Verify package | rpm -Vp pckg | dpkg -V pckg
Verify all  Packages | rpm -Va | dpkg -V
Import GPG key | rpm --import keyfile | apt-key add key file
List all GPG keys | rpm -qa gpg-pubkey* | apt-key list
Rebuild corrupted database | 