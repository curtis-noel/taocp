FROM centos:latest

RUN yum -y install wget glibc atk pango fribidi glib2 gtk2-devel \
    && yum -y groupinstall "Development tools" \
    && wget http://ftp.gnu.org/gnu/mdk/v1.2.10/mdk-1.2.10.tar.gz \
    && tar xfvz mdk-1.2.10.tar.gz \
    && cd mdk-1.2.10 \
    && ./configure \
    && make \
    && make install \
    && cd .. \
    && rm -rf mdk-1.2.10.tar.gz \
    && yum -y update \
    && yum -y clean all
CMD ["/bin/bash"]
