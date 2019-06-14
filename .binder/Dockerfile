FROM rocker/binder:3.5.2
LABEL maintainer='Anna'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}
RUN wget https://github.com/annakrystalli/testdrive-holepunch/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2019-01-01/')); devtools::install_deps()"
