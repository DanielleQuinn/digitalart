FROM rocker/binder:3.6.3
LABEL maintainer='Unknown'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}



RUN wget https://github.com/DanielleQuinn/digitalart/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2020-07-15/')); devtools::install_deps(); devtools::install_github('djnavarro/flametree')"

RUN rm DESCRIPTION.1; exit 0
