# һ��ǰ��
Docker ��������Ƽ���������ֵ��¼�����Ŀǰ��Docker ������Ϊ�����������������ȶ��Ѿ��Ĺ���֮ǰ�� OpenStack��Docker �Լ������������������������У���ʹ��Ϊ���������Ľ�������������������Ƽ��������������������˼�롣�����Ļ���������ҵӦ�ÿ�������΢����� DevOps ������˼����Ϊ�������ġ��� Docker �����ĳ��ֺ����������������������̬Ȧ��չ�Ĵٽ�����������΢����� DevOps ������˼��ʵ���еĺܶ����⣬ʹ��ǰ������˼����ģ��ʵ�ֳ�Ϊ�˿��ܡ����ԣ������б�Ҫ�������˽�һ�� Docker �������������������Ƽ���ʱ����������������ʲô����Ӱ�졣

**���Ľ������������ݣ�**
1. ʲô����������
1. ʲô�� Docker
1. Docker �����ʵ�ֵ�
1. ΪʲôҪʹ�� Docker

���� Docker ���÷����������������ܡ�Docker ������ʹ�ã�����ǰ�� Docker ���������ָ߼��÷������ɡ����飬����ǰ��������վ CSDN��InfoQ �� CoreOS��Centurylink Labs ����Щʹ�� Docker ���Ƽ��㳧�̵���վ��

# ���������������
����������ʱ�ᱻ��Ϊ���������⼼��������ͬ�ڻ��� Hypervisor �Ĵ�ͳ���⻯������������������������Ӳ�������������������ڵĽ��̶������������� Linux ϵͳ���ں�֮�ϡ�����ֱ�����еĽ��̲�ͬ�������������ڵĽ��̻ᱻ�����Լ�����Ӷ���ֱ�����еĸ�Чʵ�������⼼���Ĵ󲿷�Ч����
 
![�ڴ�����ͼƬ����][1]

## ������������ʷ 
��������������һ�������������1979����ֵ��� Unix ϵͳ�е� chroot �������������ĳ��Ρ��������ֵ� BSD Jail��Solaris Containers �� OpenVZ ����������������������������������ʼ�ռ�ȴ����2007�꣬��һ�� Google ���׳� cgroups�����Ҵ� 2.6.4 ��ʼ��Linux �ں˰�������һ������������������ʼ���ռ�������������������������Ҫ�ȵ�2013�� Docker 0.10 �汾������
 
# ����Docker ���
�� Docker ����֮ǰ������ Google ����ʹ���������������ڵ����Ա�Ҳʹ��������������Լ���Ӧ��ƽ̨��Ӱ�������Ŀ�Դ PaaS ������� CloudFoundry��Ҳ��ʹ���Լ�������������� Warden���� Docker ����֮�����伫�п��ܳ�Ϊδ����ҵӦ�á�������Ӧ�ú��Ƽ���Ӧ�õĿ�������������Ľ�ɫ�����Եõ��˼������е�ҵ����е�׷����Google��VMware��΢����RedHat �ȵȶ���ȫ���ƶ� Docker �����ķ�չ��ͬʱ��Χ�� Docker��������һϵ���� CoreOS Ϊ�������¼�����

Docker �ĳ��ֲ��Ǵ�����һ���µ����������������� LXC (LinuX Container)<sup>ע1</sup>��cgroups��namespaces ����֮����������һ�ּ�����
 
* Docker �������������У���ͨ��һ���򵥵�������ܹ�������һ������ `docker run [params] [image] [command (optional)]`
* Docker ������������Ĺ����ͷַ���Docker �ṩ�� `Dockerfile` �� `docker commit` ���ַ�ʽ�������񣬲����ṩ�� Docker image registry �����Ա���ͷַ�����
 
## ����ؽ���
��һ���ȷ�����װ�䣨����������Զ�����䣨Ӧ�����У���˵ʮ����Ҫ����װ�䣨�������ܱ������Ӧ�ã������䲻���໥��ײ��Ӧ�ó�ͻ�����𻵣�Ҳ�ܱ��ϵ�һЩΣ�ջ��﷢����ģ����ı�ը��Ӧ�ñ�����ʱ���Შ���������Ӧ�ã����ǰѻ��Ӧ�ã�װ���ڼ�װ�䣨�������в�����һ���򵥵����顣����ɫ����ͷ���ˣ�Docker���ĳ��ֽ������һ���⡣����Docker��ʹ�û���װ�ص���װ�䣨��������һ���̱������׾١�����Զ�����䣨Ӧ�����У����ԣ��ö���С���֣������������ԭ���Ĵ���֣�ʵ�����Ҳ�ܱ�֤���Ӧ�ã��˴�֮��İ�ȫ�����Ǻͼ�װ�䣨�������ȣ��ɱ����ߣ����ʺ�����ĳЩ��Ҫ���Ӧ�ã���
 
![�ڴ�����ͼƬ����][2]

# �ġ�Docker �����
Docker ��Ҫ�� Docker Hub �� Docker ������ɡ�ǰ����Docker �ٷ��ṩ����������ֿ⣻�����������������ϣ��ɷ�Ϊ�������˺Ϳͻ��������֡��������˸��𹹽������кͷַ� Docker ��������Ҫ�������ͻ��˸�������û�������ͷ���������ͨ�š�

![�ڴ�����ͼƬ����][3]

�����������֣�Dockerfile Ҳ�ǲ��ò���ģ�����Ȼ��������һ�����������������ȴ�� Docker �к���Ҫ�Ĳ��֡�ͨ�� Dockerfile��������Ա���Դ����Լ��� Docker ��������Dockerfile �������ӿ�������ά�����������ã��ǳ��������� DevOps �ĳ�����

## Docker Hub
Docker Hub �� Docker �ٷ����ṩ��һ������ֿ⡣������ Docker �����򹹽��Լ�����������ʱ������ֱ�ӻ��ӵ�ʹ�õ� Docker Hub �еľ���

## Docker Engine
Docker Engine ������ Docker ��������������������ͣ��Docker ����Ĺ����ȹ��ܵȹ��ܡ������ǽӴ�����������������򵥽���һ�� Docker ���������

* `run` ����һ��������������񲻴����������ء����ò����� `-d`��`-t`��`-i` ��
* `pull` ������������
* `start/stop` ����/ֹͣһ�� Docker ����
* `rm` ɾ��һ������
* `rmi` ɾ��һ����������
* `commit` �������е��޸��ύ��������
* `logs` ��ʾ�������еĿ���̨���
* `build` �� Dockerfile ����һ������
* `inspect` ��ʾ�������в�����ͨ������һ�� JSON ��ʽ��ֵ����ʾ��Ӧ�Ľ��
* `images` ��ʾ��ǰ�������ϵ����о���

## Dockerfile
ͨ����д Dockerfile�����ǿ��Թ����Լ��ľ��񡣿�һ�� Dockerfile �����ӣ�
```
FROM dockerfile/java:oracle-java8
MAINTAINER Lifan Yang <yanglifan@gmail.com>
ADD device.jar /device.jar
EXPOSE 8080
ENTRYPOINT java -jar /device.jar
```
`FROM` ָ�����˼��˵��ľ����ǻ���һ��ʲô����`dockerfile/java:oracle-java8` ��һ����������֣���Ҳ����һ���������񹷹�������ʵ��Ҳ�ǻ������� Ubuntu��CentOS ������ Base ���񡣹��� Base ���������������Docker �������н��ܣ���Ҫר�ŵĹ��ߣ����ﲻ�������ܡ�`MAINTAINER` ָ���ǿ�ѡ�ġ�`ADD` ָ����������һ���ļ���Ŀ¼���ӵ� Docker �����У�ǰ����Դ�ļ���������Ŀ���ļ���Դ�ļ�����ʹ�����·����`EXPOSE` ָ�����������䱩¶�˿ڣ���ָ���Ķ˿�Ҳ�ᱻ `-P` ����ӳ�����������һ������˿��ϡ�`ENTRYPOINT` ��������ָ������ Docker ����ʱ����������ִ�е�������ʲô�������Ҫ���ж���������ͨ�� [Supervisor](https://docs.docker.com/articles/using_supervisord/) ��ִ�С�

������Щָ�����һЩ���õ�ָ����磬�����ڹ���������ִ������� `CMD` ָ����������������û��������� `ENV` ָ���ϸ��� [Dockerfile Reference](https://docs.docker.com/reference/builder/)
 
# �塢Docker ��ʵ��

������Ҫ���� Docker ��ʹ�õļ�����Ҫ������namespaces��cgroups��LXC �� AUFS��

## namespaces
Linux ����ͨ�� Kernel �� namespaces ������Ϊһ����һ����̴��������� `pid`��`net` �� namespaces���Ӷ������������໥���롣���潫���� namespaces �������Щ��Դ���з��������ʵ���໥���룺
 
### `pid` namespace 
��ͬ�����н�����ͨ�� pid namespace ���뿪�ģ��Ҳ�ͬ�����п�������ͬ pid��������������:

* ÿ�� namespace �е� pid �����Լ��� pid=1 �ĳ�ʼ����
* ÿ�� namespace �еĽ���ֻ��Ӱ���Լ���ͬһ�� namespace ���� namespace �еĽ���
* ��Ϊ `/proc` �����������еĽ��̣�����������е� `/proc` Ŀ¼ֻ�ܿ����Լ� namespace �еĽ���
* ��Ϊ namespace ����Ƕ�ף��� namespace ����Ӱ���� namespace �Ľ��̣������� namespace �Ľ��̿����ڸ� namespace �п��������Ǿ��в�ͬ�� pid
 
### `net` namespace
������������˽��̿ռ䣬���ǻ������⡣����������ڶ������������ Apache ����������ֻ����һ��������ʹ�� 80 �˿ڡ��Դ���������ѡ����ÿ�� Apache ������ʹ�ò�ͬ�Ķ˿ڣ����߸�������ռ䡣

`net` namespace ʹ��ÿ�����������Լ��� `lo` loopback �ӿڡ�ͬʱ������һ��ͨ��������Ϊ `eth0` ������ӿڣ�ͨ������ӿڣ��������Ժ� host ��������������ͨ�š�`eth0` interface �ᱻ����һ�� 172.17.0.XXX �� IP ��ַ������֮�����ͨ����� IP ��ַ�໥ͨ�š�

![�ڴ�����ͼƬ����][4]
**ͼ3��**�����ڲ� `ifconfig` ����鿴�Ľ��

ͬʱ����������� `eth0` ������ Host �е�������һ������ `vethdfb7` �����ԹŹֵ����֡����������� `docker0` �����Ž���һ��

![�ڴ�����ͼƬ����][5]

### `ipc` namespace
`ipc` namepace ���ڲ���Ϥ Unix ���ˣ�����֮ǰ���ң����������Ǻܴ󡣱Ͼ������ڽ���֮���ͨ�Ŷ�����ͨ������ʵ�ֵġ���ʵ���ϣ�Unix `ipc` ����ʮ�ֹ㷺��Ӧ�ã�����ܵ����� `ipc` ��һ�֡��� `ipc` �Ͳ�����������ˣ���֮ Linux Kernel namespaces �����ò�ͬ������ `ipc` �໥���롣

### `mnt` namespace
������ʾ��`mnt` namespace �Ǵ������ص�ġ�`mnt` namespace ����ʹ��ͬ����ӵ�в�ͬ�Ĺ��ص��ļ�ϵͳ�� root Ŀ¼����һ�� `mnt` namespace ���ص��ļ�ϵͳֻ�ܱ�ͬһ�� namespace ��Ľ���������
 
### `uts` namespace 
`uts` namespace ���ڿ��� hostname �ĸ��롣

�������ϼ��ָ��룬һ�������Ϳ��Զ���չ�ֳ�һ����������������������Ҳ�ͬ�����ڵ���Դ�ڲ���ϵͳ����ʵ���˸��롣 Ȼ����ͬ namespace ֮����Դ�����໥�����ģ���Ȼ��Ҫ���� ulimit ������ÿ����������ʹ�õ���Դ - Docker ���õ��� cgroup��
 
�ο�����
[1] http://blog.dotcloud.com/under-the-hood-linux-kernels-on-dotcloud-part
 
## cgroups
namespaces �Խ��̷�����ʵ����Դ���룬������뻹�ǲ����ġ�һ�����̿���ͨ��ռ�ù��ȵ�Ӳ����Դ�ķ�ʽȥӰ����һ�������еĽ��̡����ԣ�Ҫ��ʵ�����Ƶ���Դ���룬����Ҫ����Դ���飬��Ҫ�ܶ���һ���ڵĽ�����ʹ�õ���Դ����Լ����cgroups ��������ʵ�����Ŀ�ĵġ�cgroups ��ȫ���� Control Groups���� 2003 ���� Google �Ĺ���ʦʵ�֣��� 2007 ����� Linux Kernel��cgroups �����ƽ��̶� CPU���ڴ桢��洢�������ʹ�á����ﲻ�� cgroups ��ʹ�÷��������ܣ�����Ȥ��ͬѧ���Բο����£�

* [SysAdminCasts.com: Introduction to Linux Control Groups (Cgroups)](https://sysadmincasts.com/episodes/14-introduction-to-linux-control-groups-cgroups)
* [Docker.com: Runtime Metrics](https://docs.docker.com/articles/runmetrics/)

��Ȼ cgroups �ṩ�˶� IO ��Դʹ�õ�Լ���Ĺ��ܣ��� Docker Ŀǰ(1.3)��δ�ṩ֧�֡�

### �ڴ�
cgroups ���Կ��ƽ�������ʹ�õ��ڴ�� swap �ռ�Ĵ�С��ͨ�� `-m` ������Docker ����������������ʹ�õ�����ڴ�����
```
docker run -m 128m -d container_img cmd_name
```

### CPU
Docker ����ͨ�� cgroups ������������ʹ�õ� CPU ��Դ����ִ�� `docker run` ����ʱ����ͨ������ `--cpu-shares` (`-c`)��`--cpuset` �� CPU �������ơ�

#### `--cpu-shares` (`-c`)
`-c` ���õ���һ��**���ֵ**�����ֵ��Ӱ�쵽�������ڵĽ�������ʹ�õ� CPU ʱ��Ƭ�������е� Docker ����Ĭ��ʹ�� 1024����һ�������� Docker ��������˵�����ֵû���κ����塣���������� Docker ������ʱ��������������ƽ�� CPU ʱ��Ƭ���������������һ����ָ�� `-c`����һ������Ϊ `-c 512`����ǰ�߽�ʹ�ô��� 2/3 �ļ�����������һ����ʹ�ô��� 1/3 �ļ������������� `-c` ����������ʹ�� CPU ������Ƶ�ʵ�û���κ�Ӱ�졣

#### `--cpuset`
������ָ�� Docker �����еĽ��������ڵڼ��� CPU �ϡ������һ��������ö��ŷָ��Ķ������ `0,1,2`���������������ʹ������������ڵ�һ�� CPU �����ϡ�
```
docker run -i -t --cpuset 0 ubuntu:14.04
```

*ע��cgroups ʹ�õ���һ��α�ļ�ϵͳ��ʽ�Ľӿڡ����α�ļ�ϵͳʵ�ʴ������ڴ��У���ӳ����Ŀ¼�С��û�ͨ�������Ŀ¼��д���ļ����� cgroups ���в�����*

## AUFS
*ע�����µ� Docker ʹ�� BTRFS ��� AUFS������Ҫʵ�ֵĹ�����ͬ*
AUFS ��ȫ���� Another Union File System��AUFS���������� UFS����һ����Ҫ��������ʹ����Ŀ¼�ṹ�϶�Ϊһ������ʲô���أ�Docker �ľ������ж������ɵģ����ϲ���һ���ɶ�д�ģ�������Ĳ�����ֻ���ġ�ͨ�� AUFS ��Ŀ¼�ںϵ�������ʵ���˼ȿ������д���ֱ�֤���²�����ݰ�ȫ��Ŀ�ġ�����ͼ������һ���������ʶ����ͼ�е� bootfs ������� Linux Kernel����������ĳ���ض��� Linux ���а汾�Ĳ�ͬ�� Kernel ���ļ��㣬����ͼ���� Debian���������а��� emacs �� Apache �������㡣��Щ������������ʱ����ֻ���ġ������������������ʱ�ɶ�д�Ĳ��ˡ�����Ĳ����ֻ����������Ĳ�����ļ��������Ĳ�νṹ����ͨ�� Dockerfile ��������

![�ڴ�����ͼƬ����][6]

��������һ���ṹ��ʲô���ĺô��أ���Ҫ�����漸�㣺

### ��ʡ���̺��ڴ�Ĵ洢�ռ�
��ʡ���̴洢�ռ�����Ϊ��ͬ����������֮����Թ�����ͬ�Ĳ㡣���磬������ͬ�� Java Ӧ�õ������������Ƕ��ǻ��� Ubuntu 14.04 �� JDK7������ͬһ̨ Host �У�����������ͻ�ʹ����ͬ�� Ubuntu 14.04 �� JDK7 �Ĳ㡣

��ʡ�ڴ�ռ�����Ϊ Linux Ϊ�˼ӿ���̷��ʣ��ὫһЩ�����ϵ��ļ����ص��ڴ��С����ԣ���ʡ���̿ռ��ͬʱҲ�Ϳ��Լ�ӵؽ����ڴ��ʹ�á�

### �ӿ첿���ٶ�
ͬ�����ɹ����ľ�����ܼӿ첿���ٶȡ���Ϊ��ͬ�Ĳ㲻�ñ��ظ����ز���

### �������ļ�����Ķ�
�ϴ��ɶ�д�Ĳ���Զ������ֻ�����е��ļ��������޸ģ�������ʵ�� copy-on-write�����ԣ������޸Ķ�����Ĳ���ʵ�ǰ�ȫ�ġ�

# ����Docker ����̬Ȧ
Docker �ٺã����� Docker �������޷����㻥��������ҵӦ�õĸ��ָ�������ġ����� Docker �ĳ��ִ�����һЩ�м����ķ�չ���γ���һ���Ӵ��[��̬Ȧ](http://www.mindmeister.com/389671722/docker-ecosystem)�������̬Ȧ�еĲ�Ʒ�ɴ��·�Ϊ���¼��ࣺ

## �������Ź���
�� Google Kubernets �� Apache Mesos Ϊ��������Ҫ�������������ɷֲ�ʽ��ȺӦ�õĹ������������������������״̬�ļ�ء������Զ����Ĺ��ϻָ�������������Ӧ�õ����ݺ����ݡ������֡�

## ���������Ĳ���ϵͳ
�� CoreOS �� Redhat Atomic Ϊ���������������� Linux ���洫ͳ�İ��������ƣ���ʹ�� Docker ��ΪӦ�õ�����ƽ̨��ͬʱ����ϵͳ��CoreOS �������� Ectd��Fleet ������Ը��õ�֧�ֲַ�ʽϵͳ��

## ����������ƽ̨
PaaS ƽ̨����ʲô���ʵĸ����ȴһֱ���ڷ���������״̬��Docker �ĳ��ָ� PaaS �ķ�չ�������µĻ�����Docker ʹ�� PaaS Ӧ�õĲ�������ͳһ�ĸ�ʽ���� Flynn �� Deis Ϊ�������µ� PaaS ����ƽ̨������ Docker Ϊ�����ġ�

## ����
����һ̨��������������Ӧ��������ǧ�� Docker ����ͬʱ���������С������������һ����������Ⱥ�е� Docker �������ж��١��������ô��� Docker ������ʹ�õ����������֯�������Ϊ�µ���ս�������������Ҫ�� Pipework��Weave �� Flannel �ȼ���

## ���ù�������
�� Puppet��Ansible ���������ù����������� Docker ����֮ǰ���ѱ��㷺ʹ�ã��� Docker �ĳ��ָ���Щ�����������µı仯���Ƿ��ܸ��õ�֧�ֶ� Docker ������Ⱥ�����ù�����������Щ�������ķ�չ��

# �ߡ��ܽ�
���ļ򵥽����� Docker ���ֵı��������壬Docker ����ɺͱ���ļ����Լ�������������̬Ȧ������Ϊһ���³��ֲ��ڿ��ٷ�չ�Ļ����Եļ�����һ��ƪ������Ȼֻ��������һ�����������ʶ��ͬʱ���κμ���Ҳ�����������ԣ�Docker ��Ϊһ���¼�����ʵ����Ҳ��������ǳ�������⡣�����ڹ��⣬Docker ��Ӧ��Ҳ�ǳ����𲽽׶Ρ����Ի��кܳ���·Ҫ�ߡ����Ǵ����һ���ķ�չ����Docker ������һ���ǳ����������ļ������ض����ڽ���һ��ʱ���ڳ�Ϊһ�����š������ļ�����

��Ȼ Docker �ĳ��ָ�����Ǹı��˷�����Ӧ�õĲ������ά������Ϊ��������˵���������ά��ģ�ͻ�Կ���Ҳ�������ش��Ӱ�죬���� Docker �ĳ�����ʹ������Ա���õز��뵽��ά�������⽫��ʹӦ�ø��졢���õص����ͷ�����

����Ҫ���ǣ��Ƽ������������δ������������ҵӦ�õķ�չ���򣬶� Docker ������������������������δ��һ��ʱ���ڳ�Ϊ�Ƽ���Ļ����Լ�����������Ƕ�������Docker ������ÿһ����ҵ��Ա�����˽������������յ�һ�ż�����


  [1]: http://static.oschina.net/uploads/space/2014/1231/185336_4TLb_1158769.jpg
  [2]: http://static.oschina.net/uploads/space/2014/1231/185402_u1jv_1158769.jpg
  [3]: http://static.oschina.net/uploads/space/2014/1231/185423_hU94_1158769.png
  [4]: http://static.oschina.net/uploads/space/2014/1231/185518_7V88_1158769.png
  [5]: http://static.oschina.net/uploads/space/2014/1231/185602_HLA9_1158769.png
  [6]: http://static.oschina.net/uploads/space/2014/1231/185612_4cys_1158769.png