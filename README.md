                                                                                                     
┌──(user㉿kali)-[~]
└─$ open https://git-scm.com
                                                                                                     
┌──(user㉿kali)-[~]
└─$ export GITHUB_USERNAME=yatskovivan
                                                                                                     
┌──(user㉿kali)-[~]
└─$ export GITHUB_EMAIL=player1111xdd08@gmail.com
                                                                                                     
┌──(user㉿kali)-[~]
└─$ export GITHUB_TOKEN=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
                                                                                                     
┌──(user㉿kali)-[~]
└─$ alias edit='subl'
                                                                                                     
┌──(user㉿kali)-[~]
└─$ cd ${GITHUB_USERNAME}/workspace
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace]
└─$ source scripts/activate                                  
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace]
└─$ mkdir ~/.config
mkdir: cannot create directory ‘/home/user/.config’: Файл существует
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace]
└─$ ls -l         
итого 20
drwxrwxr-x 6 user user 4096 окт 24  2017 node
drwxrwxr-x 5 user user 4096 июн 11 05:51 projects
drwxrwxr-x 5 user user 4096 июн 11 05:21 reports
drwxrwxr-x 2 user user 4096 июн 11 03:53 scripts
drwxrwxr-x 4 user user 4096 июн 11 05:07 tasks
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace]
└─$ cat > ~/.config/hub <<EOF
github.com:
- user: ${GITHUB_USERNAME}
  oauth_token: ${GITHUB_TOKEN}
  protocol: https
EOF
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace]
└─$ git config --global hub.protocol https   
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace]
└─$ cd projects/lab02        
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ git init
Переинициализирован существующий репозиторий Git в /home/user/yatskovivan/workspace/projects/lab02/.git/
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ git config --global user.name ${GITHUB_USERNAME}
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ git config --global user.email ${GITHUB_EMAIL}
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ git config -e --global
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab02.git
error: внешний репозиторий origin уже существует
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ git pull origin master
fatal: couldn't find remote ref master
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ git pull origin main  
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 9 (delta 0), reused 6 (delta 0), pack-reused 0 (from 0)
Распаковка объектов: 100% (9/9), 2.00 КиБ | 2.00 МиБ/с, готово.
Из https://github.com/yatskovivan/lab02
 * branch            main       -> FETCH_HEAD
 * [новая ветка]     main       -> origin/main
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ touch README.md 
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ git status
Текущая ветка: master
нечего коммитить, нет изменений в рабочем каталоге
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ git push origin main  
error: src refspec main ничему не соответствует
error: не удалось отправить некоторые ссылки в «https://github.com/yatskovivan/lab02.git»
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ git push origin master
Username for 'https://github.com': yatskovivan
Password for 'https://yatskovivan@github.com': 
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'master' on GitHub by visiting:
remote:      https://github.com/yatskovivan/lab02/pull/new/master
remote: 
To https://github.com/yatskovivan/lab02.git
 * [new branch]      master -> master
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ git pull origin master
Из https://github.com/yatskovivan/lab02
 * branch            master     -> FETCH_HEAD
Уже актуально.
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ git log               
commit 490ebba551bf9c3415b5a96abe0383f9753cd30a (HEAD -> master, origin/master, origin/main)
Author: yatskovivan <player1111xdd08@gmail.com>
Date:   Wed Jun 11 05:06:00 2025 +0300

    added .gitignore

commit 7de618bf76d76a12f3dd88adf550eb45ca8245d1
Author: yatskovivan <player1111xdd08@gmail.com>
Date:   Wed Jun 11 04:52:34 2025 +0300

    added README.md

commit 405e524868336fa037281de8429b0689cb3bcefe
Author: yatskovivan <player1111xdd08@gmail.com>
Date:   Wed Jun 11 04:35:57 2025 +0300

    Initial commit
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ mkdir sources
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ mkdir include
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ mkdir examples
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ cat > sources/print.cpp <<EOF
#include <print.hpp>

void print(const std::string& text, std::ostream& out)
{
  out << text;
}

void print(const std::string& text, std::ofstream& out)
{
  out << text;
}
EOF
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ cat > include/print.hpp <<EOF
#include <fstream>
#include <iostream>
#include <string>

void print(const std::string& text, std::ofstream& out);
void print(const std::string& text, std::ostream& out = std::cout);
EOF
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ cat > examples/example1.cpp <<EOF
#include <print.hpp>

int main(int argc, char** argv)
{
  print("hello");
}
EOF
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ cat > examples/example2.cpp <<EOF
#include <print.hpp>

#include <fstream>

int main(int argc, char** argv)
{
  std::ofstream file("log.txt");
  print(std::string("hello"), file);
}
EOF
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]
└─$ edit README.md
                                                                                                     
┌──(user㉿kali)-[~/yatskovivan/workspace/projects/lab02]