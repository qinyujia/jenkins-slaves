FROM registry.cn-beijing.aliyuncs.com/qinyujia-test/jenkins-slave-dind-java:latest

ENV GRADLE_VERSION 2.6

WORKDIR /usr/bin
RUN curl -sLO https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-all.zip && \
  unzip gradle-${GRADLE_VERSION}-all.zip && \
  ln -s gradle-${GRADLE_VERSION} gradle && \
  rm gradle-${GRADLE_VERSION}-all.zip

ENV GRADLE_HOME /usr/bin/gradle
ENV PATH $PATH:$GRADLE_HOME/bin

CMD ["/usr/sbin/sshd", "-D"]
