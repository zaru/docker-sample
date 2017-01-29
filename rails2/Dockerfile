FROM ruby:latest

ENV LANG C.UTF-8

RUN apt-get update && \
        apt-get install -y nodejs && \
        vim \
        build-essential \
        curl \
        git-core \
        libcurl4-openssl-dev \
        libreadline-dev \
        libssl-dev \
        libxml2-dev \
        libxslt1-dev \
        libyaml-dev \
        zlib1g-dev

RUN gem install bundler

ENV APP_ROOT /usr/src/docker-rails-test
WORKDIR $APP_ROOT

ADD Gemfile Gemfile
ADD Gemfile.lock Gemfile.lock
RUN bundle config without test development doc
RUN bundle install
ADD . /docker-rails-test
