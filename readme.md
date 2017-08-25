# shortUrl
一个生成短链接的 Laravel 扩展。

## 安装

```shell
$ composer require xbb/shorturl
```

## 配置

1. 添加下面一行到 `config/app.php` 中 `providers` 部分：

    ```php
    Xbb\shortUrl\shortUrlServiceProvider::class,
    ```

2. 发布迁移文件

    ```php
    $ php artisan vendor:publish --provider='Xbb\shortUrl\shortUrlServiceProvider'
    ```

3. 迁移数据库表

    ```php
    $ php artisan migrate
    ```

4. 使用

    ```php
    app('shortUrl')->makeShortUrl($url);
 
    header('Location:'.app('shortUrl')->hit($shortUrl));
    ```


# License

MIT