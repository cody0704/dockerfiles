FROM centos:6

RUN yum -y install wget

# Update glibc
RUN wget -q http://copr-be.cloud.fedoraproject.org/results/mosquito/myrepo-el6/epel-6-x86_64/glibc-2.17-55.fc20/glibc-2.17-55.el6.x86_64.rpm \
    && wget -q http://copr-be.cloud.fedoraproject.org/results/mosquito/myrepo-el6/epel-6-x86_64/glibc-2.17-55.fc20/glibc-common-2.17-55.el6.x86_64.rpm \
    && wget -q http://copr-be.cloud.fedoraproject.org/results/mosquito/myrepo-el6/epel-6-x86_64/glibc-2.17-55.fc20/glibc-devel-2.17-55.el6.x86_64.rpm \
    && wget -q http://copr-be.cloud.fedoraproject.org/results/mosquito/myrepo-el6/epel-6-x86_64/glibc-2.17-55.fc20/glibc-headers-2.17-55.el6.x86_64.rpm \
    && wget -q https://copr-be.cloud.fedoraproject.org/results/mosquito/myrepo-el6/epel-6-x86_64/glibc-2.17-55.fc20/glibc-utils-2.17-55.el6.x86_64.rpm \
    && wget -q https://copr-be.cloud.fedoraproject.org/results/mosquito/myrepo-el6/epel-6-x86_64/glibc-2.17-55.fc20/glibc-static-2.17-55.el6.x86_64.rpm \
    && rpm -Uh --force --nodeps \
        glibc-2.17-55.el6.x86_64.rpm \
        glibc-common-2.17-55.el6.x86_64.rpm \
        glibc-devel-2.17-55.el6.x86_64.rpm \
        glibc-headers-2.17-55.el6.x86_64.rpm \
        glibc-static-2.17-55.el6.x86_64.rpm \
        glibc-utils-2.17-55.el6.x86_64.rpm \
    && rm *.rpm

# Update libstdc++
RUN  wget -q https://copr-be.cloud.fedoraproject.org/results/mosquito/myrepo-el6/epel-6-x86_64/gcc-4.8.2-16.3.fc20/libstdc++-4.8.2-16.3.el6.x86_64.rpm \
    && wget -q https://copr-be.cloud.fedoraproject.org/results/mosquito/myrepo-el6/epel-6-x86_64/gcc-4.8.2-16.3.fc20/libstdc++-devel-4.8.2-16.3.el6.x86_64.rpm \
    && wget -q https://copr-be.cloud.fedoraproject.org/results/mosquito/myrepo-el6/epel-6-x86_64/gcc-4.8.2-16.3.fc20/libstdc++-static-4.8.2-16.3.el6.x86_64.rpm \
    && rpm -Uh \
        libstdc++-4.8.2-16.3.el6.x86_64.rpm \
        libstdc++-devel-4.8.2-16.3.el6.x86_64.rpm \
        libstdc++-static-4.8.2-16.3.el6.x86_64.rpm \
    && rm *.rpm

# Set the default shell to bash instead of sh
ENV SHELL /bin/bash
