FROM ruby:2.3.1

MAINTAINER Harsh Vakharia <harshjv@gmail.com>

ENV APP_HOME /app

RUN apt-get update && \
    apt-get install -y build-essential libpq-dev libxml2-dev \
                       libxslt1-dev libmagickwand-dev libjpeg-dev \
                       libpng-dev libgmp3-dev libqtwebkit-dev \
                       qt4-qmake libqt4-webkit libqt4-dev xvfb \
                       advancecomp gifsicle jhead jpegoptim libjpeg-progs \
                       optipng pngcrush pngquant \
                       libcurl4-openssl-dev \
                       libedit-dev libssl-dev libxml2-dev \
                       xz-utils libsqlite3-dev sqlite3 \
                       git curl vim nano \
                       postgresql-client redis-tools && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN echo "gem: --no-ri --no-rdoc" > ~/.gemrc

RUN gem install rake bundler rails

RUN mkdir $APP_HOME

WORKDIR $APP_HOME

CMD ["true"]
