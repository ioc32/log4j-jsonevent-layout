# CEE-enabled `json_event` pattern for log4j

## What is it?
This fork enables CEE/lumberjack output support. It basically clones the original log4j-jsonevent-layout classes and appends the CEE cookie to the resulting JSON structure.
Please take a look at the upstream project for documentation.

# Usage
This is just a quick snippit of a `log4j.properties` file:

```
log4j.rootCategory=WARN, RollingLog
log4j.appender.RollingLog=org.apache.log4j.DailyRollingFileAppender
log4j.appender.RollingLog.Threshold=TRACE
log4j.appender.RollingLog.File=api.log
log4j.appender.RollingLog.DatePattern=.yyyy-MM-dd
log4j.appender.RollingLog.layout=net.logstash.log4j.JSONEventLayoutCEE
```
