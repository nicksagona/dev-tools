# Dev Tools

A collection of dev tools based in BASH. Includes helper scripts for:

* [Git](#git)
* [Composer](#composer)
* [PHP](#php)

It is recommended to copy the scripts to a folder in the `$PATH` environment variable.

### Git

##### Git Fetch Origin

```bash
$ gf
```

##### Git Rebase Origin

Rebase to the current branch on origin

```bash
$ gr
```

##### Git Pull Origin

Pull origin down to the current branch

```bash
$ gpo
```

##### Git Fetch & Rebase Origin

Fetch and rebase to the current branch on origin

```bash
$ gro
```

##### Git Checkout Branch

```bash
$ gco branch
```

##### Git Create Branch

```bash
$ gcb branch
```

##### Git List Branches

Local branches

```bash
$ gbr
```
Remote branches

```bash
$ gbr -r
```

All branches

```bash
$ gbr -a
```

##### Git Delete Branch

Delete local branch

```bash
$ gbr -d branch
```

Delete remote branch

```bash
$ gbr -rd branch
```

Delete both local and remote branches

```bash
$ gbr -dd branch
```

##### Git Prune Origin

```bash
$ gpr
```

##### Git Merge

```bash
$ gm branch
```

##### Git Commit

```bash
$ gc "Message"
```

##### Git Push

```bash
$ gp
```

##### Git Commit and Push

```bash
$ gcp "Message"
```


##### Git Status

```bash
$ gs
```

##### Git Stash

```bash
$ gst
```

##### Git Stash Pop

```bash
$ gpop
```

##### Git List Tags

```bash
$ gt
```

##### Git Delete Tag

Delete local tag

```bash
$ gt -d tag
```

Delete remote tag

```bash
$ gt -rd tag
```

Delete both local and remote tags

```bash
$ gt -dd tag
```

[Top](#dev-tools)

### Composer

##### Install Composer

```bash
$ ci
```

##### Update Composer

```bash
$ cu
```

##### Require Composer Package

```bash
$ cr popphp/popphp
```

##### Clear Composer Cache

```bash
$ ccc
```

##### Remove Composer Installation

This will remove the `composer.lock` file and `vendor` folder:

```bash
$ crm
```

Remove and clear the cache 

```bash
$ crm -c
```

[Top](#dev-tools)

### PHP

##### Switch PHP Versions

Use only if you have multiple versions of php in the `/usr/bin/` folder and `/usr/bin/php`
is a symbolic link. It will manage the current version by deleting the symbolic link
and creating a new one:

``` text
lrwxrwxrwx /usr/bin/php -> /usr/bin/php8.2
-rwxr-xr-x /usr/bin/php7.3
-rwxr-xr-x /usr/bin/php7.4
-rwxr-xr-x /usr/bin/php8.1
-rwxr-xr-x /usr/bin/php8.2
```

If Apache is utilized, it will attempt to set the correct Apache PHP module and restart Apache.

Switch to an available version of PHP on the system:

```bash
$ sudo phpsw 8.2
```

##### Start the PHP Server

Start `localhost:8000` in the current directory:

```bash
$ phpsrv
```

Start `localappdomain:8080` in the `public` directory:

```bash
$ phpsrv public localappdomain 8080
```

[Top](#dev-tools)
