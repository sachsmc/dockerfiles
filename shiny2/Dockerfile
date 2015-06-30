FROM rocker/shiny

MAINTAINER Michael Sachs "sachsmc@gmail.com"

RUN apt-get update && apt-get install -y \
	libxml2-dev  
	
RUN R -e "install.packages(c('gridSVG', 'ggthemes', 'plotROC'), repos='http://cran.rstudio.com/')"

RUN cp -R /usr/local/lib/R/site-library/shiny/examples/* /srv/shiny-server/

EXPOSE 3838

CMD ["/usr/bin/shiny-server.sh"]