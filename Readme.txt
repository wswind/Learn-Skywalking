http://skywalking.apache.org/downloads/
https://github.com/SkyAPM/SkyAPM-dotnet
https://www.cnblogs.com/landonzeng/p/10616644.html

openjdk

yum install java-1.8.0-openjdk

elasticsearch

https://www.elastic.co/cn/downloads/elasticsearch

https://mirrors.huaweicloud.com/elasticsearch

https://www.elastic.co/guide/en/elasticsearch/reference/7.6/rpm.html#rpm-repo

下载 https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-7.6.2-x86_64.rpm
rpm -iv elasticsearch-7.6.2-x86_64.rpm


/etc/elasticsearch/elasticsearch.yml

sudo journalctl --unit elasticsearch

GET /

{
  "name" : "Cp8oag6",
  "cluster_name" : "elasticsearch",
  "cluster_uuid" : "AT69_T_DTp-1qgIJlatQqA",
  "version" : {
    "number" : "7.6.2",
    "build_flavor" : "default",
    "build_type" : "tar",
    "build_hash" : "f27399d",
    "build_date" : "2016-03-30T09:51:41.449Z",
    "build_snapshot" : false,
    "lucene_version" : "8.4.0",
    "minimum_wire_compatibility_version" : "1.2.3",
    "minimum_index_compatibility_version" : "1.2.3"
  },
  "tagline" : "You Know, for Search"
}

/opt/apache-skywalking-apm-bin-es7/config/application.yml

/opt/apache-skywalking-apm-bin-es7/bin/startup.sh

http://192.168.56.10:8080/

https://github.com/SkyAPM/SkyAPM-dotnet/issues/292


%appdata%\NuGet\NuGet.Config

add MyGet
https://www.myget.org/F/skyapm-dotnet/api/v3/index.json

dotnet add package SkyAPM.Agent.AspNetCore

"ASPNETCORE_HOSTINGSTARTUPASSEMBLIES": "SkyAPM.Agent.AspNetCore",
"SKYWALKING__SERVICENAME": "BFF"

dotnet tool install -g SkyAPM.DotNet.CLI
dotnet skyapm config sample_app 192.168.56.10:11800


