Cloudflare API v4 Dynamic DNS Update in Bash, without unnecessary requests
Now the script also supports v6(AAAA DDNS Recoards)


-----


这个脚本在路由器上运行报错，改了一下

#### 测试环境：
**ARM**  
**BusyBox v1.19.4**



#### 修改内容：
- BusyBox V1.19  unsupported 【grep -P】
- The log file cannot be created


#### 文件系统只读问题
在路由器上将文件复制到 /usr/local/bin 报错
```
/usr# mkdir local
mkdir: can't create directory 'local': Read-only file system
```
以读写方式重新挂载根目录
```
mount -o remount rw /

```
