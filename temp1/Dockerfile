FROM ubuntu:18.04

RUN apt-get update && apt-get install -y git vim curl unzip gcc make wget tar bzip2 subversion bison flex openssl libssl-dev wget sudo

RUN echo "Installing Ruby"

RUN cd /root && wget http://cache.ruby-lang.org/pub/ruby/2.7/ruby-2.7.1.tar.gz && tar zxf ruby-2.7.1.tar.gz && cd ruby-2.7.1

RUN cd /root/ruby-2.7.1 && ./configure && make && sudo -E make install
ENV PATH /usr/local/bin:$PATH
RUN ruby -v

CMD ["ruby","-v"]

