+++
date = "2015-05-11T03:05:44+09:00"
draft = false
title = "[Mac] Homebrewインストールログ"
tags = ["Mac"]
+++

<div><div><b>Homebrew</b>とは、Mac上のアプリケーションパッケージを管理するソフトです<br /><br />詳しくはこちら↓↓↓に書かれているのですが、自分のメモとログを残します<br /><br /></div>＊MacにHomebrewをインストールする - Qiita</div><div><a  target="_blank" href="http://qiita.com/is0me/items/475fdbc4d770534f9ef1">http://qiita.com/is0me/items/475fdbc4d770534f9ef1</a><br /><br />＊Homebrewの本家<br /><a  target="_blank" href="http://brew.sh/">http://brew.sh/</a><br /><br />Macでのインストールログ<br /></div><blockquote><div><div><span  style="color: rgb(255, 0, 255);">## Homebrew入ってない状態</span></div></div><div><div>MacProSao:~ Sao$ brew</div></div><div><div>-bash: brew: command not found</div></div><div><div>&nbsp;</div></div><div><div><span  style="color: rgb(255, 0, 255);">## VIMでバッシュプロファイル作成</span></div></div><div><div>MacProSao:~ Sao$ <span  style="color: rgb(255, 0, 255);">vim .bash_profile</span></div></div><br /><div><div>MacProSao:~ Sao$ <span  style="color: rgb(255, 0, 255);">more .bash_profile&nbsp;</span></div></div><div><div><span  style="color: rgb(255, 0, 255);">export PATH=/usr/local:$PATH</span></div></div><br /><div><div>MacProSao:~ Sao$ pwd</div></div><div><div>/Users/Sao</div></div><br /><div><div><span  style="color: rgb(255, 0, 255);">## /usr/local の作成&nbsp;</span></div></div><div><div>MacProSao:usr Sao$ <span  style="color: rgb(255, 0, 255);">sudo mkdir /usr/local/</span></div></div><br /><div><div>WARNING: Improper use of the sudo command could lead to data loss</div></div><div><div>or the deletion of important system files. Please double-check your</div></div><div><div>typing when using sudo. Type "man sudo" for more information.</div></div><br /><div><div>To proceed, enter your password, or type Ctrl-C to abort.</div></div><br /><div><div>Password:</div></div><div><div>MacProSao:usr Sao$ ls -al</div></div><div><div>total 8</div></div><div><div>drwxr-xr-x@ &nbsp; 12 root &nbsp;wheel &nbsp; &nbsp;408 &nbsp;5 11 02:24 .</div></div><div><div>drwxr-xr-x &nbsp; &nbsp;30 root &nbsp;wheel &nbsp; 1088 &nbsp;5 11 02:17 ..</div></div><div><div>drwxr-xr-x &nbsp; &nbsp; 5 root &nbsp;wheel &nbsp; &nbsp;170 &nbsp;9 10 &nbsp;2014 X11</div></div><div><div>lrwxr-xr-x &nbsp; &nbsp; 1 root &nbsp;wheel &nbsp; &nbsp; &nbsp;3 &nbsp;2 22 18:01 X11R6 -&gt; X11</div></div><div><div>drwxr-xr-x &nbsp;1053 root &nbsp;wheel &nbsp;35802 &nbsp;5 &nbsp;2 23:30 bin</div></div><div><div>drwxr-xr-x &nbsp; 257 root &nbsp;wheel &nbsp; 8738 &nbsp;5 11 01:25 include</div></div><div><div>drwxr-xr-x &nbsp; 271 root &nbsp;wheel &nbsp; 9214 &nbsp;5 11 01:25 lib</div></div><div><div>drwxr-xr-x &nbsp; 170 root &nbsp;wheel &nbsp; 5780 &nbsp;4 26 13:43 libexec</div></div><div><div>drwxr-xr-x &nbsp; &nbsp; 2 root &nbsp;wheel &nbsp; &nbsp; 68 &nbsp;5 11 02:24 local</div></div><div><div>drwxr-xr-x &nbsp; 244 root &nbsp;wheel &nbsp; 8296 &nbsp;4 26 13:40 sbin</div></div><div><div>drwxr-xr-x &nbsp; &nbsp;44 root &nbsp;wheel &nbsp; 1496 &nbsp;5 11 01:25 share</div></div><div><div>drwxr-xr-x &nbsp; &nbsp; 4 root &nbsp;wheel &nbsp; &nbsp;136 &nbsp;2 22 17:56 standalone</div></div><br /><div><div><span  style="color: rgb(255, 0, 255);">## Homebrewのインストール</span></div></div><div><div>MacProSao:usr Sao$ <span  style="color: rgb(255, 0, 255);">ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"</span></div></div><div><div>==&gt; This script will install:</div></div><div><div>/usr/local/bin/brew</div></div><div><div>/usr/local/Library/...</div></div><div><div>/usr/local/share/man/man1/brew.1</div></div><div><div>==&gt; The following directories will be made group writable:</div></div><div><div>/usr/local/.</div></div><div><div>==&gt; The following directories will have their group set to admin:</div></div><div><div>/usr/local/.</div></div><br /><div><div>Press RETURN to continue or any other key to abort</div></div><div><div>==&gt; /usr/bin/sudo /bin/chmod g+rwx /usr/local/.</div></div><div><div>==&gt; /usr/bin/sudo /usr/bin/chgrp admin /usr/local/.</div></div><div><div>==&gt; /usr/bin/sudo /bin/mkdir /Library/Caches/Homebrew</div></div><div><div>==&gt; /usr/bin/sudo /bin/chmod g+rwx /Library/Caches/Homebrew</div></div><div><div>==&gt; Downloading and installing Homebrew...</div></div><div><div>remote: Counting objects: 3572, done.</div></div><div><div>remote: Compressing objects: 100% (3421/3421), done.</div></div><div><div>remote: Total 3572 (delta 35), reused 1459 (delta 18), pack-reused 0</div></div><div><div>Receiving objects: 100% (3572/3572), 2.72 MiB | 2.47 MiB/s, done.</div></div><div><div>Resolving deltas: 100% (35/35), done.</div></div><div><div>From https://github.com/Homebrew/homebrew</div></div><div><div>&nbsp;* [new branch] &nbsp; &nbsp; &nbsp;master &nbsp; &nbsp; -&gt; origin/master</div></div><div><div>HEAD is now at c007efc Riak 2.1.1</div></div><div><div>==&gt; Installation successful!</div></div><div><div>==&gt; Next steps</div></div><div><div>Run `brew help` to get started</div></div><br /><div><div><span  style="color: rgb(255, 0, 255);">## プロファイル読み込み&nbsp;</span></div></div><div><div>MacProSao:~ Sao$ <span  style="color: rgb(255, 0, 255);">source .bash_profile</span>&nbsp;</div></div><br /><div><div><span  style="color: rgb(255, 0, 255);">## バージョン確認</span></div></div><div><div>MacProSao:~ Sao$ <span  style="color: rgb(255, 0, 255);">brew -v</span></div></div><div><div><span  style="color: rgb(255, 0, 255);">Homebrew 0.9.5</span></div></div><div><div>&nbsp;</div></div><div><div>MacProSao:~ Sao$&nbsp;</div></div></blockquote>
<div>Hugoを入れるためにインストールしてみました<br />ついにわたしもGoを使う日が来るなんて…(ﾟ∇ﾟ ;)</div>