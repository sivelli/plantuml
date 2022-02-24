FROM openjdk:17-alpine
ENV PLANTUML_VERSION=1.2022.1
ENV LANG en_US.UTF-8
RUN apk add --no-cache graphviz ttf-droid ttf-droid-nonlatin
RUN wget "http://downloads.sourceforge.net/project/plantuml/${PLANTUML_VERSION}/plantuml.${PLANTUML_VERSION}.jar" -O plantuml.jar

ENTRYPOINT ["java", "-DPLANTUML_LIMIT_SIZE=8196", "-Djava.awt.headless=true", "-jar", "plantuml.jar"]
CMD ["-p", "-tsvg"]
