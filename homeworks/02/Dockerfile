FROM ruby:3.0.0-alpine
    
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

COPY ./Gemfile /usr/src/app/
RUN bundle install
COPY ./ /usr/src/app
ENV RACK_ENV production
EXPOSE 80

CMD ["rackup", "config.ru", "--host", "0.0.0.0", "--port", "80"]