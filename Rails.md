## Rails
-  see [https://guides.rubyonrails.org/getting_started.html](https://guides.rubyonrails.org/getting_started.html) 
-  see [https://www.bilibili.com/video/BV1wb411z7Pq?from=search&seid=3583598220673653830](https://www.bilibili.com/video/BV1wb411z7Pq?from=search&seid=3583598220673653830) 

## install ruby with devkit
## install sqlite3, install the sqlite3 gem
-  had to do this cause "rails new xxx" fails with sqlite3 gem 
-  install MinGW (as sqlite3 requires c compiler), add path 
-  see [https://stackoverflow.com/questions/15480381/how-do-i-install-sqlite3-for-ruby-on-windows](https://stackoverflow.com/questions/15480381/how-do-i-install-sqlite3-for-ruby-on-windows) 
-  Download and extract the autoconf package from Sqlite.org (also dll-win32, tools-win32, 3 zips in total) 
-  Run msys.bat (it is inside the ruby devkit root folder)(not the exact file name, but the ruby devkit (.exe)) 
-  cd into the path where you downloaded the sqlite source (for example: "cd /c/dev/sqlite3" for path "c:\dev\sqlite3" if you are new to MSYS/MINGW32) 
-  Run "./configure" 
-  Run "make" 
-  Run "make install" 
-  add sqlite3 path 
-  Get the sqlite3 gem again, this time specifying the platform and the path to the newly compiled binaries:"gem install sqlite3 --platform=ruby -- --with-sqlite3-include=/c:/sqlite3/ --with-sqlite3-lib=/c:/sqlite3/.libs/" 

## install node.js, install yarn

## gem install rails, wait really long time

## rails new blog, wait when 'bundle install' (important)
- no need to modify gemfile version info

## trying to render local index page, having trouble with webpack
-  see [https://blog.csdn.net/qq_38111015/article/details/79013475](https://blog.csdn.net/qq_38111015/article/details/79013475) 
-  see [https://classic.yarnpkg.com/en/package/webpack](https://classic.yarnpkg.com/en/package/webpack) 
-  below are awful attempts that worked after put together 
   -  do it in the nodejs folder (not sure), add webpacker path 
   -  i did: npm install webpack -g; yarn add webpack-cli 
   -  for JSON ERROR see [https://www.cnblogs.com/sansancn/p/11139030.html](https://www.cnblogs.com/sansancn/p/11139030.html) 
   -  for ERRNO -4048 see [https://blog.csdn.net/long870294701/article/details/81703987](https://blog.csdn.net/long870294701/article/details/81703987) 
   -  for r/w permission issue, manually set all permission [caution] 
   -  see [https://github.com/rails/webpacker/issues/217](https://github.com/rails/webpacker/issues/217) 
   -  "Error: Cannot find module '@rails/webpacker'" 
   -  i did: rails: webpacker:install 
   -  finally done! 

-  guess the right things to do are: 
   -  cd the rails project 
   -  npm install xxxxx 
   -  rails: webpacker:install 
