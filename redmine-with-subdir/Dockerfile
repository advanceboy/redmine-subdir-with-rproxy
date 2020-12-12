FROM redmine:4-alpine

# re-write config.ru for running in the sub-URI 
# https://www.redmine.org/issues/32318
RUN sed -i -e "s/\(\s*run Rails.*$\)/\nmap ENV\['RAILS_RELATIVE_URL_ROOT'\] || '\/' do\n  \1\nend/g" \
    /usr/src/redmine/config.ru
