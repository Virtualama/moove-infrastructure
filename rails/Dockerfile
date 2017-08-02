FROM ruby:2.4.1
RUN apt-get update -qq && apt-get install -y nodejs

RUN mkdir /myapp
WORKDIR /myapp

ADD ./app/Gemfile* /myapp/
ADD ./bin/* /bin/
RUN chmod +x /bin/*

RUN bundle -j4
RUN pwd
RUN ls


# ENTRYPOINT ["bundle", "exec", "rails", "s", "-p", "3000", "-b", "'0.0.0.0'"]
# RUN useradd -u 1000 -m www-bridge-user
# COPY ../app /myapp
# ADD Gemfile /myapp/Gemfile
# ADD Gemfile.lock /myapp/Gemfile.lock
# CMD /bin/sh -c bundle
