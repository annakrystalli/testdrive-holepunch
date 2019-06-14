FROM rocker/binder:3.3.2
LABEL maintainer='karthik'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}
RUN wget https://github.com/annakrystalli/testdrive-holepunch/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2017-01-01/')); devtools::install_deps()"
