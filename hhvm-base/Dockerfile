FROM centos:centos7
MAINTAINER Steven Edwards <steven@stephenwithav.com>

RUN yum -y install epel-release

RUN yum -y install cpp gcc-c++ cmake git psmisc {binutils,boost,jemalloc}-devel \
    {sqlite,tbb,bzip2,openldap,readline,elfutils-libelf,gmp,lz4,pcre}-devel \
    lib{xslt,event,yaml,vpx,png,zip,icu,mcrypt,memcached,cap,dwarf}-devel \
    {unixODBC,expat,mariadb}-devel lib{edit,curl,xml2,xslt}-devel \
    glog-devel oniguruma-devel ocaml gperf enca libjpeg-turbo-devel make

ADD https://github.com/facebook/hhvm/archive/HHVM-3.7.1.tar.gz /tmp/

WORKDIR /tmp

RUN tar xzf HHVM-3.7.1.tar.gz
