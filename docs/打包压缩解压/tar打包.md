# tar打包

## 命令格式

```
Usage: tar [OPTION...] [FILE]...
GNU 'tar' saves many files together into a single tape or disk archive, and can
restore individual files from the archive.
```

## 举例

```
Examples:
  tar -cf archive.tar foo bar  # Create archive.tar from files foo and bar.
  tar -tvf archive.tar         # List all files in archive.tar verbosely.
  tar -xf archive.tar          # Extract all files from archive.tar.
```

```
tar \
	--exclude=.git --exclude='.gitignore' --exclude='.gitmodules' \
	 \
	--exclude=FreeBSD --exclude=debian --exclude=rpm --exclude=rump --exclude=apk \
	--transform="s,/build/VERSION,VERSION,S" \
	--transform="s,,msgpuck-2.0.12/,S" \
	--owner=root --group=root \
	-T /build/ls-lR.txt --show-transformed \
	-caPf /build/msgpuck-2.0.12.tar.xz /build/VERSION
```

* --exclude= # 指定排除的文件所在的路径
  - ```-X, --exclude-from=FILE    exclude patterns listed in FILE```
* --transform=EXPRESSION, --xform=EXPRESSION # 使用sed匹配修改文件名
  - ```--transform=EXPRESSION, --xform=EXPRESSION use sed replace EXPRESSION to transform file names```
* --owner=root # 强制属主
  - ```--owner=NAME           force NAME as owner for added files```
* --group=root # 强制属组
  - ```--owner=NAME           force NAME as group for added files```
* -T
  - ```-T, --files-from=FILE      get names to extract or create from FILE```
* --show-transformed
* -a # 根据目标文件后缀自动启用压缩
  - ```-a, --auto-compress        use archive suffix to determine the compression program```
* -f
  - ```-f, --file=ARCHIVE         use archive file or device ARCHIVE```
* -P
  - ```-P, --absolute-names       don't strip leading '/'s from file names```




























---
