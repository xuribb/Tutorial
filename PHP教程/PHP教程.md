##### 

# PHP教程

版本：1.0.0

最后更新时间：2025-07-03

作者：陆家伟

## 循环结构

### 1. for

### 2. while

### 3. do...while

### 4. foreach





## 常量

### 1. 魔术常量

- `__LINE__` - 文件中的当前行号

- `__FILE__` - 文件的完整路径和文件名

- `__DIR__` - 文件所在的目录

- `__FUNCTION__` - 函数名称

- `__CLASS__` - 类的名称

- `__TRAIT__` - Trait 的名称

- `__METHOD__` - 类的方法名称

- `__NAMESPACE__` - 当前命名空间的名称

### 2. 标准预定义常量

- `PHP_VERSION` - 当前 PHP 版本

- `PHP_MAJOR_VERSION` - PHP 主版本号

- `PHP_MINOR_VERSION` - PHP 次版本号

- `PHP_RELEASE_VERSION` - PHP 发布版本号

- `PHP_VERSION_ID` - PHP 版本号，整数形式

- `PHP_EXTRA_VERSION` - PHP 额外版本信息

- `PHP_ZTS` - 是否线程安全 (1 for yes, 0 for no)

- `PHP_DEBUG` - 是否调试版本 (1 for yes, 0 for no)

- `PHP_MAXPATHLEN` - PHP 支持的最大路径长度

- `PHP_OS` - 运行 PHP 的操作系统

- `PHP_OS_FAMILY` - 操作系统家族 (Windows, Linux, BSD, Darwin 等)

- `PHP_SAPI` - 服务器 API 类型 (如 "cli", "apache2handler", "fpm-fcgi" 等)

- `PHP_EOL` - 当前平台的换行符

- `PHP_INT_MAX` - 整数最大值

- `PHP_INT_MIN` - 整数最小值

- `PHP_INT_SIZE` - 整数字节大小

- `PHP_FLOAT_DIG` - 浮点数精度位数

- `PHP_FLOAT_EPSILON` - 最小可表示的浮点数

- `PHP_FLOAT_MIN` - 最小可表示的浮点数

- `PHP_FLOAT_MAX` - 最大可表示的浮点数

- `DEFAULT_INCLUDE_PATH` - 默认包含路径

- `PEAR_INSTALL_DIR` - PEAR 安装目录

- `PEAR_EXTENSION_DIR` - PEAR 扩展目录

- `PHP_EXTENSION_DIR` - PHP 扩展目录

- `PHP_PREFIX` - PHP 安装前缀

- `PHP_BINDIR` - PHP 二进制文件目录

- `PHP_BINARY` - PHP 二进制路径

- `PHP_MANDIR` - PHP man 页面目录

- `PHP_LIBDIR` - PHP 库目录

- `PHP_DATADIR` - PHP 数据目录

- `PHP_SYSCONFDIR` - PHP 系统配置目录

- `PHP_LOCALSTATEDIR` - PHP 本地状态目录

- `PHP_CONFIG_FILE_PATH` - PHP 配置文件路径

- `PHP_CONFIG_FILE_SCAN_DIR` - PHP 额外配置文件扫描目录

- `PHP_SHLIB_SUFFIX` - 共享库后缀 (如 "so" 或 "dll")

- `PHP_FD_SETSIZE` - select 系统调用支持的最大文件描述符数

### 3. 错误报告常量

- `E_ERROR` (1) - 致命运行时错误

- `E_WARNING` (2) - 运行时警告

- `E_PARSE` (4) - 编译时解析错误

- `E_NOTICE` (8) - 运行时通知

- `E_CORE_ERROR` (16) - PHP初始化启动时的致命错误

- `E_CORE_WARNING` (32) - PHP初始化启动时的警告

- `E_COMPILE_ERROR` (64) - 致命编译时错误

- `E_COMPILE_WARNING` (128) - 编译时警告

- `E_USER_ERROR` (256) - 用户生成的错误

- `E_USER_WARNING` (512) - 用户生成的警告

- `E_USER_NOTICE` (1024) - 用户生成的通知

- `E_STRICT` (2048) - 运行时通知，启用 PHP 对代码的修改建议

- `E_RECOVERABLE_ERROR` (4096) - 可捕获的致命错误

- `E_DEPRECATED` (8192) - 运行时通知，启用后将会对在未来版本中可能无法正常工作的代码给出警告

- `E_USER_DEPRECATED` (16384) - 用户生成的警告信息

- `E_ALL` (32767) - 所有错误和警告

### 4. 布尔常量

- `TRUE` - 表示真值

- `FALSE` - 表示假值

- `NULL` - 表示空值

### 5. 扩展提供的常量

PHP 的各种扩展也提供了大量特定功能的常量。

###### 文件系统相关

- `DIRECTORY_SEPARATOR` - 目录分隔符 (Windows 是 "", Unix 是 "/")

- `PATH_SEPARATOR` - 路径分隔符 (Windows 是 ";", Unix 是 ":")

###### 日期时间相关

- `DATE_ATOM` - Atom 格式日期 (如: 2023-01-01T12:00:00+00:00)

- `DATE_COOKIE` - HTTP Cookie 格式日期

- `DATE_ISO8601` - ISO-8601 格式日期

- `DATE_RFC822` - RFC 822 格式日期

- `DATE_RFC850` - RFC 850 格式日期

- `DATE_RFC1036` - RFC 1036 格式日期

- `DATE_RFC1123` - RFC 1123 格式日期

- `DATE_RFC2822` - RFC 2822 格式日期

- `DATE_RFC3339` - RFC 3339 格式日期

- `DATE_RFC7231` - RFC 7231 格式日期

- `DATE_RSS` - RSS 格式日期

- `DATE_W3C` - W3C 格式日期

## 函数大全

###### parse_url

```php
$query_string = parse_url($url, PHP_URL_QUERY);
```

###### parse_str

```php
parse_str($query_string, $params);
var_dump($params);
```

###### explode

```php
$data = explode("&", "a=1&b=2&c=3", 3);
```

###### count

```php
$data = count(['a','b']);
```

###### urlencode

```php
$url = urlencode("https://www.baidu.com/?a=1&b=2");
```

###### urldecode

```php
$url = urldecode("https%3A%2F%2Fwww.baidu.com%2F%3Fa%3D1%26b%3D2");
```

###### print_r

```php
print_r(['a', 'b']);
```

###### var_dump

```php
var_dump(['a', 'b']);
```

###### http_build_query

```php
$query = [
    'a' => 1,
    'b' => 2
];
$query_string = http_build_query($query);
```

###### array_map

```php
$data = [
    'a' => 1,
    'b' => 2
];
function n2($val){
    return $val * $val;
}
$data = array_map("n2", $data);
print_r($data);
```

###### substr

```php
$res = substr($str, 2);
$res = substr($str, 2, 2);
$res = substr($str, -6);
```

###### mb_substr

```php
$str = "こんにちは世界";

$sub = mb_substr($str, 0, 5, 'UTF-8'); // "こんにちは"
```

###### strstr

```php
$res = strstr($str, 'flag');
$res = strstr($str, 'flag', true);
```

###### preg_match

```php
preg_match('/php/i', 'php is a progress language.');
preg_match('/^php(.*)/i', 'php is a progress language.', $matches);
```

###### strtok

```php
$str = "first=John&last=Doe&age=30";

$token = strtok($str, "=&");
while ($token !== false) {
    echo $token . "\n";
    $token = strtok("=&");
}
```

###### file_exists

###### function_exists

```php
if (!function_exists('mb_substr')) {
    die('mbstring 扩展未安装');
}
```

###### file_get_contents

```php
$content = file_get_contents('filename.txt');
```

###### openssl_pkey_get_private

```php
$privateKey = openssl_pkey_get_private($keyContent, $passphrase);
```

###### openssl_error_string

```php
$error = openssl_error_string();
```

###### openssl_sign

```php
openssl_sign($data, $signature, $privateKey, OPENSSL_ALGO_SHA256);
```

###### openssl_free_key

```php
openssl_free_key($privateKey);
```

###### openssl_verify

```php
openssl_verify($testData, $signature, $publicKey, OPENSSL_ALGO_SHA256)
```

###### openssl_pkey_new

###### base64_encode

###### base64_decode

###### openssl_pkey_get_details

###### bin2hex

###### hex2bin



### 数组相关

- array_key_first()

- array_key_last()

- array_is_list()

- array_contains()

- array_partition()

- array_unique()

- array_filter()

- array_map()

- array_chunk

- array_column()



## PSR PHP标准推荐

### 1. 简介

PSR 是由 PHP FIG 组织制定的 PHP 规范，是 PHP 开发的实践标准。

### 2.

## PHP扩展和包体系

### 1. PHP 扩展（Extensions）

PHP 扩展是用 C 编写的，直接集成到 PHP 核心中，提供底层功能支持。它们可以分为以下几种：

- ###### 核心扩展（Core Extensions）
  
  随 PHP 官方发行版内置，默认启用
  
  示例：`PDO`、`JSON`、`mbstring`、`openssl`、`session`

- ###### 外部扩展（PECL 扩展）
  
  通过 [PECL](https://pecl.php.net/)（PHP Extension Community Library）安装
  
  需要手动编译或使用 `pecl install` 安装
  
  示例：`xdebug`、`redis`、`swoole`、`imagick`

- ###### Zend 扩展（Zend Extensions）
  
  比普通 PHP 扩展更底层，可以修改 PHP 引擎行为
  
  示例：`OPcache`、`Xdebug`、`ionCube`

### 2. PHP 包（Packages）

PHP 包是纯 PHP 代码的库，通常用于业务逻辑，而不是底层功能。它们可以分为以下几种：

- ###### PEAR 包（已逐渐淘汰）
  
  通过 `pear install` 全局安装
  
  示例：`PHP_CodeSniffer`、`Mail_Mime`

- ###### Composer 包（现代 PHP 标准）
  
  通过 `composer.json` 管理依赖，安装到 `vendor/` 目录

- ###### 框架专用包
  
  某些 PHP 框架（如 Laravel、Symfony）有自己的包管理系统

- ###### PHAR 包（PHP Archive）
  
  单个 `.phar` 文件，类似 Java 的 `.jar`
  
  示例：`phpunit.phar`、`composer.phar`

### 3. 总结

| 类型             | 语言  | 安装方式               | 适用场景                 |
| -------------- | --- | ------------------ | -------------------- |
| **PHP 核心扩展**   | C   | 内置 PHP             | 基础功能（如 `PDO`）        |
| **PECL 扩展**    | C   | `pecl install`     | 高性能扩展（如 `swoole`）    |
| **Zend 扩展**    | C   | 编译安装               | 引擎级修改（如 `OPcache`）   |
| **PEAR 包**     | PHP | `pear install`     | 旧式全局库（已淘汰）           |
| **Composer 包** | PHP | `composer require` | 现代 PHP 开发（如 Laravel） |
| **PHAR 包**     | PHP | 直接下载               | 独立工具（如 PHPUnit）      |

## Composer

### 1. 基本使用

###### 初始化init

```powershell
composer init
```

###### 安装所有声明的依赖

```powershell
composer install
```

###### 更新依赖

```powershell
composer update [单个包名]
composer upgrade [单个包名]
```

###### 安装指定的依赖

```powershell
composer require [单个包名]
```

###### 删除指定的依赖

```powershell
composer remove [单个包名]
```

###### 查看包

```powershell
composer show             // 查看当前项目下所有包
composer show --platform  // 查看系统平台包
```

###### 重新生成autoload.php

```powershell
composer dump-autoload
composer dump
```

###### 查看所以命令列表

```powershell
composer list
```

###### 列出当前项目配置

```powershell
composer config --list   // 查看所有配置项
```

###### 清理缓存

```powershell
composer clear-cache     // 删除缓存目录中一切
```
