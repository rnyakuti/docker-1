FROM ruby:latest

RUN apt-get update && apt-get upgrade -y && apt-get install -y nodejs && gem install rails bundler

ONBUILD WORKDIR /opt
ONBUILD RUN rails new app

ONBUILD WORKDIR /opt/app
ONBUILD RUN bundle install
ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed