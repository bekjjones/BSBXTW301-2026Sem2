#VMware how-to guide for CLI (Command Line Interface) to connect to a GitHub Repo

##COMMANDS

###INSTALL GITHUB & GIT, LOGIN & CLONE REPO
```
sudo apt install gh
sudo apt install git
gh auth login
gh repo clone <account_name>/<repo_name>
```
###INSTALL A COMMAND LINE EDITOR
```
sudo apt install vim
```

###EDIT A FILE THEN COMMIT & PUSH TO GITHUB REPO
```
vim test.html
git add .
git commit
git push origin
```

##INFO ABOUT EACH COMMAND & EXAMPLES

```
sudo apt install gh
```
*What to expect following*
```
[sudo] password for devops: 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages were automatically installed and are no longer required:
  libfwupd2 libfwupdplugin5 libgcab-1.0-0 libsmbios-c2
Use 'sudo apt autoremove' to remove them.
The following NEW packages will be installed:
  gh
0 to upgrade, 1 to newly install, 0 to remove and 144 not to upgrade.
Need to get 6,242 kB of archives.
After this operation, 33.7 MB of additional disk space will be used.
Get:1 http://au.archive.ubuntu.com/ubuntu jammy/universe amd64 gh amd64 2.4.0+dfsg1-2 [6,242 kB]
Fetched 6,242 kB in 0s (13.1 MB/s)
Selecting previously unselected package gh.
(Reading database ... 214532 files and directories currently installed.)
Preparing to unpack .../gh_2.4.0+dfsg1-2_amd64.deb ...
Unpacking gh (2.4.0+dfsg1-2) ...
Setting up gh (2.4.0+dfsg1-2) ...
Processing triggers for man-db (2.10.2-1) ...
devops@devops-virtual-machine:~$ gh auth login
? What account do you want to log into? GitHub.com
? What is your preferred protocol for Git operations? SSH
? Generate a new SSH key to add to your GitHub account? (Y/n) 
```


```
sudo apt install git
```
*What to expect following*
```
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages were automatically installed and are no longer required:
  libfwupd2 libfwupdplugin5 libgcab-1.0-0 libsmbios-c2
Use 'sudo apt autoremove' to remove them.
The following additional packages will be installed:
  git-man liberror-perl
Suggested packages:
  git-daemon-run | git-daemon-sysvinit git-doc git-email git-gui gitk gitweb git-cvs git-mediawiki git-svn
The following NEW packages will be installed:
  git git-man liberror-perl
0 to upgrade, 3 to newly install, 0 to remove and 144 not to upgrade.
Need to get 4,154 kB of archives.
After this operation, 21.0 MB of additional disk space will be used.
Do you want to continue? [Y/n] 
Get:1 http://au.archive.ubuntu.com/ubuntu jammy/main amd64 liberror-perl all 0.17029-1 [26.5 kB]
Get:2 http://au.archive.ubuntu.com/ubuntu jammy-updates/main amd64 git-man all 1:2.34.1-1ubuntu1.17 [954 kB]
Get:3 http://au.archive.ubuntu.com/ubuntu jammy-updates/main amd64 git amd64 1:2.34.1-1ubuntu1.17 [3,174 kB]
Fetched 4,154 kB in 0s (12.9 MB/s)
Selecting previously unselected package liberror-perl.
(Reading database ... 214648 files and directories currently installed.)
Preparing to unpack .../liberror-perl_0.17029-1_all.deb ...
Unpacking liberror-perl (0.17029-1) ...
Selecting previously unselected package git-man.
Preparing to unpack .../git-man_1%3a2.34.1-1ubuntu1.17_all.deb ...
Unpacking git-man (1:2.34.1-1ubuntu1.17) ...
Selecting previously unselected package git.
Preparing to unpack .../git_1%3a2.34.1-1ubuntu1.17_amd64.deb ...
Unpacking git (1:2.34.1-1ubuntu1.17) ...
Setting up liberror-perl (0.17029-1) ...
Setting up git-man (1:2.34.1-1ubuntu1.17) ...
Setting up git (1:2.34.1-1ubuntu1.17) ...
Processing triggers for man-db (2.10.2-1) ...
```

```
gh auth login
```

*What to expect following*
```
? What account do you want to log into? GitHub.com
? What is your preferred protocol for Git operations? HTTPS
? Authenticate Git with your GitHub credentials? Yes
? How would you like to authenticate GitHub CLI? Login with a web browser

! First copy your one-time code: DCEC-FF74
- Press Enter to open github.com in your browser... ^C
devops@devops-virtual-machine:~$ gh auth login
? What account do you want to log into? GitHub.com
? What is your preferred protocol for Git operations? HTTPS
? Authenticate Git with your GitHub credentials? Yes
? How would you like to authenticate GitHub CLI? Login with a web browser

! First copy your one-time code: A241-4DBC
- Press Enter to open github.com in your browser... 
VMware: No 3D enabled (0, Success).
VMware: No 3D enabled (0, Success).
VMware: No 3D enabled (0, Success).
VMware: No 3D enabled (0, Success).
VMware: No 3D enabled (0, Success).
VMware: No 3D enabled (0, Success).
[5306:7:0730/144631.725505:ERROR:gpu/ipc/client/command_buffer_proxy_impl.cc:285] ContextResult::kTransientFailure: Failed to send GpuControl.CreateCommandBuffer.
Created TensorFlow Lite XNNPACK delegate for CPU.
[5215:5243:0730/144635.291940:ERROR:google_apis/gcm/engine/registration_request.cc:291] Registration response error message: DEPRECATED_ENDPOINT
[5215:5243:0730/144656.169943:ERROR:google_apis/gcm/engine/registration_request.cc:291] Registration response error message: DEPRECATED_ENDPOINT
[5258:5303:0730/144707.106213:ERROR:components/viz/service/display/display.cc:272] Frame latency is negative: -0.031 ms
[5258:5303:0730/144708.137601:ERROR:components/viz/service/display/display.cc:272] Frame latency is negative: -0.171 ms
[5215:5215:0730/144715.452073:ERROR:mojo/public/cpp/bindings/lib/interface_endpoint_client.cc:748] Message 5 rejected by interface blink.mojom.WidgetHost
[5258:5303:0730/144715.751329:ERROR:components/viz/service/display/display.cc:272] Frame latency is negative: -0.062 ms
✓ Authentication complete. Press Enter to continue...
[5215:5243:0730/144751.701237:ERROR:google_apis/gcm/engine/registration_request.cc:291] Registration response error message: DEPRECATED_ENDPOINT

- gh config set -h github.com git_protocol https
✓ Configured git protocol
✓ Logged in as bekjjones
```

```
gh repo clone bekjjones/mypracticerepo
```
*What to expect following*
```
Cloning into 'mypracticerepo'...
remote: Enumerating objects: 67, done.
remote: Counting objects: 100% (21/21), done.
remote: Compressing objects: 100% (19/19), done.
remote: Total 67 (delta 7), reused 2 (delta 0), pack-reused 46 (from 1)
Receiving objects: 100% (67/67), 14.39 KiB | 589.00 KiB/s, done.
Resolving deltas: 100% (27/27), done.
```

*View the files within the repo/current folder(aka. directory)*
```
ls
```
```
DarkMode.html   index.html                    mypracticerepo      SampleEmailSent.html  wekafiles
Desktop         index.html.1                  Pictures            snap
Documents       LiveServerTest.html           pt                  Templates
Downloads       melbourne_startup-config.txt  Public              ToggleSample.html
HelloWord.html  Music                         RSSFeedSample.html  Videos
```

*change directory - move into the repo folder*
```
cd mypracticerepo
```

*View the files within the repo/current folder(aka. directory)
```
ls
```
```
 README.md      test.html                      'test_new_file - Copy (3).txt'
'Syntax Prac'  'test_new_file - Copy (1).txt'  'test_new_file - Copy (4).txt'
 Test          'test_new_file - Copy (2).txt'   test_new_file.txt
```

##INSTALL VIM: A command line editor

```
sudo apt install vim
```
*What to expect following*
```
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages were automatically installed and are no longer required:
  libfwupd2 libfwupdplugin5 libgcab-1.0-0 libsmbios-c2
Use 'sudo apt autoremove' to remove them.
The following additional packages will be installed:
  vim-common vim-runtime vim-tiny
Suggested packages:
  ctags vim-doc vim-scripts indent
The following NEW packages will be installed:
  vim vim-runtime
The following packages will be upgraded:
  vim-common vim-tiny
2 to upgrade, 2 to newly install, 0 to remove and 142 not to upgrade.
Need to get 9,352 kB of archives.
After this operation, 37.6 MB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://au.archive.ubuntu.com/ubuntu jammy-updates/main amd64 vim-tiny amd64 2:8.2.3995-1ubuntu2.34 [707 kB]
Get:2 http://au.archive.ubuntu.com/ubuntu jammy-updates/main amd64 vim-common all 2:8.2.3995-1ubuntu2.34 [81.5 kB]
Get:3 http://au.archive.ubuntu.com/ubuntu jammy-updates/main amd64 vim-runtime all 2:8.2.3995-1ubuntu2.34 [6,831 kB]
Get:4 http://au.archive.ubuntu.com/ubuntu jammy-updates/main amd64 vim amd64 2:8.2.3995-1ubuntu2.34 [1,732 kB]
Fetched 9,352 kB in 1s (17.6 MB/s)
(Reading database ... 215633 files and directories currently installed.)
Preparing to unpack .../vim-tiny_2%3a8.2.3995-1ubuntu2.34_amd64.deb ...
Unpacking vim-tiny (2:8.2.3995-1ubuntu2.34) over (2:8.2.3995-1ubuntu2.31) ...
Preparing to unpack .../vim-common_2%3a8.2.3995-1ubuntu2.34_all.deb ...
Unpacking vim-common (2:8.2.3995-1ubuntu2.34) over (2:8.2.3995-1ubuntu2.31) ...
Selecting previously unselected package vim-runtime.
Preparing to unpack .../vim-runtime_2%3a8.2.3995-1ubuntu2.34_all.deb ...
Adding 'diversion of /usr/share/vim/vim82/doc/help.txt to /usr/share/vim/vim82/doc/help.txt.vim-tiny by 
vim-runtime'
Adding 'diversion of /usr/share/vim/vim82/doc/tags to /usr/share/vim/vim82/doc/tags.vim-tiny by vim-runt
ime'
Unpacking vim-runtime (2:8.2.3995-1ubuntu2.34) ...
Selecting previously unselected package vim.
Preparing to unpack .../vim_2%3a8.2.3995-1ubuntu2.34_amd64.deb ...
Unpacking vim (2:8.2.3995-1ubuntu2.34) ...
Setting up vim-common (2:8.2.3995-1ubuntu2.34) ...
Setting up vim-runtime (2:8.2.3995-1ubuntu2.34) ...
Setting up vim (2:8.2.3995-1ubuntu2.34) ...
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/vim (vim) in auto mode
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/vimdiff (vimdiff) in auto mode
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/rvim (rvim) in auto mode
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/rview (rview) in auto mode
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/vi (vi) in auto mode
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/view (view) in auto mode
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/ex (ex) in auto mode
Setting up vim-tiny (2:8.2.3995-1ubuntu2.34) ...
Processing triggers for mailcap (3.70+nmu1ubuntu1) ...
Processing triggers for desktop-file-utils (0.26-1ubuntu3) ...
Processing triggers for hicolor-icon-theme (0.17-2) ...
Processing triggers for gnome-menus (3.36.0-1ubuntu3) ...
Processing triggers for man-db (2.10.2-1) ...
```

EDIT A FILE
```
vim test.html
```
*Commands for editing within VIM the command line editor can be seen at the bottom of the window*

ADD, COMMIT & PUSH TO GITHUB REPO
```
git add .
git commit
git push origin
```
*provide author identity*

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

```
git config --global user.name bekjjones
git config --global user.email "randerson@sunitafe.edu.au"
```

*Commit the changes*
```
git commit
```
*What to expect following*
[master 2f01b54] Corrected style and script tags in head
 1 file changed, 21 insertions(+), 21 deletions(-)
devops@devops-virtual-machine:~/mypracticerepo$ git log
commit 2f01b542f24e00c392a203b0ea0d15cb1d7cb490 (HEAD -> master)
Author: bekjjones <randerson@sunitafe.edu.au>
Date:   Thu Jul 30 15:02:41 2026 +1000

    Corrected style and script tags in head

commit 2e5095f2a011f54cfee1a908d0a2e70fd0ff0f5c (origin/master, origin/HEAD)
Merge: 16856db 9dc1c68
Author: Rebekah Anderson <bek.j.jones@gmail.com>
Date:   Thu Jul 30 13:21:13 2026 +1000

    Merge pull request #8 from OldMateVB/patch-1
    
    Create Syntax Prac

commit 16856db6a22a2676d9e9814fb0f49aea3a21a0ae
Merge: 4b95552 af544fa
Author: Rebekah Anderson <bek.j.jones@gmail.com>
Date:   Thu Jul 30 13:20:06 2026 +1000

    Merge pull request #7 from JarradT/master
    
    add a text file

commit 9dc1c68ebf72191ef76d643b21ca9d2a61306238
Author: OldMateVB <13146440@students.sunitafe.edu.au>
Date:   Thu Jul 30 12:46:18 2026 +1000

    Create Syntax Prac
    
    Testing syntax code

commit af544fa870fcff740fe9b8d51e71808bc8418424
Author: JarradT <30029531@students.sunitafe.edu.au>
Date:   Thu Jul 30 11:40:10 2026 +1000

    Update test_new_file - Copy (4) test edit.txt

commit 08b586d45b1558203a8cceb5e43d8c485a5f2ba0
Merge: 2ff2981 4b95552

*Push the changes to the repository*
```
git push origin
```
*What to expect following*
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 443 bytes | 443.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/bekjjones/mypracticerepo.git
   2e5095f..2f01b54  master -> master
