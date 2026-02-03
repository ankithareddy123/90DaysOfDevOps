Created users & groups
Managed group memberships correctly
Set shared directories
Applied correct permissions
Tested access the right way (without switching shells)

history of commands:
    1.cat etc/passwd
    2  ls
    3  cat /etc/passwd
    4  grep -E "tokyo|berlin|professor" /etc/passwd
    5  pwd
    6  cat /etc/group
    7  usermod -aG admin berlin
    8  cat /etc/group
    9  groups berlin
   10  mkdir /opt/dev-project
   11  chgrp developers /opt/project
   12  chgrp developers /opt/dev-project
   13  chmod 775 /opt/dev-project
   14  sudo -i tokyo touch /opt/dev-project/testfile.txt
   15  sudo -u tokyo touch /opt/dev-project/testfile.txt
   16  ls -l /opt/dev-project
   17  useradd -m nairobi
   18  groupadd project-team
   19  usermod -aG project-team nairob
   20  usermod -aG project-team nairobi
   21  usermod -aG project-team tokyo
   22  mkdir /opt/team-workspace
   23  chgrp project-team /opt/team-workspace
   24  ls -ld /opt/team-workspace
   25  chmod 775 /opt/team-workspace
   26  sudo -u nairobi touch /opt/team-workspace/testfile.txt
   27  history
   
