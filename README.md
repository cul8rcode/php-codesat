# php-codesat

#### 介绍
PHP Code Static Analysis Tool
利用git hook、phplint、phpstan，在code commit的时候对php代码进行语法检测、代码风格检查，如果有问题，不允许提交。


#### 使用
composer require cul8r/php-codesat

安装成功之后执行:``composer exec php-codesat install``该命令会检查phplint、phpstan的安装情况，并将git原有的pre-commit钩子备份，再将php-codesat的pre-commit钩子拷贝至``.git/hooks``中。

这样，在git commit之前，就会执行phplint和phpstan检查待提交的文件，如果不满足要求，则会组织代码提交。

#### 指令
|指令 (composer exec -v phpsat {指令}|用法|
|----|----|
|install|安装php-codesat|
|remove|移除php-codesat|
|config|配置|

#### 注意事项
1. 建议使用最新版本，最新版本可以在仓库的tags中查看;
2. 包以提交到packagist，但是国内安装比较慢，推荐自建composer的repository来安装。



#### 注意事项
phpcc的pre-commit会覆盖原有的pre-commit，但仍然会将它备份为pre-commit.bak.{timestamp}。所以之前有在pre-commit中插入操作，请谨慎安装。

change from php-cc 
