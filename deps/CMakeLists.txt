CMAKE_MINIMUM_REQUIRED(VERSION 3.5)
PROJECT(TDengine)

ADD_SUBDIRECTORY(zlib-1.2.11)
ADD_SUBDIRECTORY(pthread)
ADD_SUBDIRECTORY(regex)
ADD_SUBDIRECTORY(iconv)
ADD_SUBDIRECTORY(lz4)
ADD_SUBDIRECTORY(cJson)
ADD_SUBDIRECTORY(wepoll)
ADD_SUBDIRECTORY(MsvcLibX)

IF (TD_LINUX AND TD_MQTT)
  ADD_SUBDIRECTORY(MQTT-C)
ENDIF ()

IF (TD_DARWIN AND TD_MQTT)
  ADD_SUBDIRECTORY(MQTT-C)
ENDIF ()
