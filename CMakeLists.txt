CMAKE_MINIMUM_REQUIRED(VERSION 2.8.10)
PROJECT(zecpp CXX)

SET(CMAKE_CXX_FLAGS "-std=c++11")

SET(OUTPUT_DIR ${CMAKE_BINARY_DIR}/bin)
SET(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${OUTPUT_DIR})
SET(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${OUTPUT_DIR})
SET(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${OUTPUT_DIR})

ADD_EXECUTABLE(asyncsrv src/asyncsrv.cpp)
TARGET_LINK_LIBRARIES(asyncsrv zmq pthread)

ADD_EXECUTABLE(hwclient src/hwclient.cpp)
TARGET_LINK_LIBRARIES(hwclient zmq)

ADD_EXECUTABLE(hwserver src/hwserver.cpp)
TARGET_LINK_LIBRARIES(hwserver zmq)

ADD_EXECUTABLE(identity src/identity.cpp src/zhelpers.hpp)
TARGET_LINK_LIBRARIES(identity zmq)

ADD_EXECUTABLE(interrupt src/interrupt.cpp)
TARGET_LINK_LIBRARIES(interrupt zmq)

ADD_EXECUTABLE(lbbroker2 src/lbbroker2.cpp)
TARGET_LINK_LIBRARIES(lbbroker2 zmq czmq)

ADD_EXECUTABLE(lbbroker src/lbbroker.cpp)
TARGET_LINK_LIBRARIES(lbbroker zmq pthread)

ADD_EXECUTABLE(lpclient src/lpclient.cpp)
TARGET_LINK_LIBRARIES(lpclient zmq)

ADD_EXECUTABLE(lpserver src/lpserver.cpp)
TARGET_LINK_LIBRARIES(lpserver zmq)

ADD_EXECUTABLE(mdbroker src/mdbroker.cpp)
TARGET_LINK_LIBRARIES(mdbroker zmq)

ADD_EXECUTABLE(mdclient2 src/mdclient2.cpp)
TARGET_LINK_LIBRARIES(mdclient2 zmq)

ADD_EXECUTABLE(mdclient src/mdclient.cpp)
TARGET_LINK_LIBRARIES(mdclient zmq)

ADD_EXECUTABLE(mdworker src/mdworker.cpp)
TARGET_LINK_LIBRARIES(mdworker zmq)

ADD_EXECUTABLE(msgqueue src/msgqueue.cpp)
TARGET_LINK_LIBRARIES(msgqueue zmq)

ADD_EXECUTABLE(mspoller src/mspoller.cpp)
TARGET_LINK_LIBRARIES(mspoller zmq)

ADD_EXECUTABLE(msreader src/msreader.cpp)
TARGET_LINK_LIBRARIES(msreader zmq)

ADD_EXECUTABLE(mtrelay src/mtrelay.cpp)
TARGET_LINK_LIBRARIES(mtrelay zmq pthread)

ADD_EXECUTABLE(mtserver src/mtserver.cpp)
TARGET_LINK_LIBRARIES(mtserver zmq pthread)

ADD_EXECUTABLE(ppqueue src/ppqueue.cpp)
TARGET_LINK_LIBRARIES(ppqueue zmq)

ADD_EXECUTABLE(ppworker src/ppworker.cpp)
TARGET_LINK_LIBRARIES(ppworker zmq)

ADD_EXECUTABLE(psenvpub src/psenvpub.cpp)
TARGET_LINK_LIBRARIES(psenvpub zmq)

ADD_EXECUTABLE(psenvsub src/psenvsub.cpp)
TARGET_LINK_LIBRARIES(psenvsub zmq)

ADD_EXECUTABLE(rrbroker src/rrbroker.cpp)
TARGET_LINK_LIBRARIES(rrbroker zmq)

ADD_EXECUTABLE(rrclient src/rrclient.cpp)
TARGET_LINK_LIBRARIES(rrclient zmq)

ADD_EXECUTABLE(rrworker src/rrworker.cpp)
TARGET_LINK_LIBRARIES(rrworker zmq)

ADD_EXECUTABLE(rtdealer src/rtdealer.cpp)
TARGET_LINK_LIBRARIES(rtdealer zmq pthread)

ADD_EXECUTABLE(rtreq src/rtreq.cpp)
TARGET_LINK_LIBRARIES(rtreq zmq pthread)

ADD_EXECUTABLE(spqueue src/spqueue.cpp)
TARGET_LINK_LIBRARIES(spqueue zmq)

ADD_EXECUTABLE(spworker src/spworker.cpp)
TARGET_LINK_LIBRARIES(spworker zmq)

ADD_EXECUTABLE(suisnail src/suisnail.cpp)
TARGET_LINK_LIBRARIES(suisnail zmq pthread)

ADD_EXECUTABLE(syncpub src/syncpub.cpp)
TARGET_LINK_LIBRARIES(syncpub zmq)

ADD_EXECUTABLE(syncsub src/syncsub.cpp)
TARGET_LINK_LIBRARIES(syncsub zmq)

ADD_EXECUTABLE(tasksink2 src/tasksink2.cpp)
TARGET_LINK_LIBRARIES(tasksink2 zmq)

ADD_EXECUTABLE(tasksink src/tasksink.cpp)
TARGET_LINK_LIBRARIES(tasksink zmq)

ADD_EXECUTABLE(taskvent src/taskvent.cpp)
TARGET_LINK_LIBRARIES(taskvent zmq)

ADD_EXECUTABLE(taskwork2 src/taskwork2.cpp)
TARGET_LINK_LIBRARIES(taskwork2 zmq)

ADD_EXECUTABLE(taskwork src/taskwork.cpp)
TARGET_LINK_LIBRARIES(taskwork zmq)

ADD_EXECUTABLE(tripping src/tripping.cpp)
TARGET_LINK_LIBRARIES(tripping zmq pthread)

ADD_EXECUTABLE(udpping1 src/udpping1.cpp)
TARGET_LINK_LIBRARIES(udpping1 zmq pthread)

ADD_EXECUTABLE(version src/version.cpp)
TARGET_LINK_LIBRARIES(version zmq)

ADD_EXECUTABLE(wuclient src/wuclient.cpp)
TARGET_LINK_LIBRARIES(wuclient zmq)

ADD_EXECUTABLE(wuproxy src/wuproxy.cpp)
TARGET_LINK_LIBRARIES(wuproxy zmq)

ADD_EXECUTABLE(wuserver src/wuserver.cpp)
TARGET_LINK_LIBRARIES(wuserver zmq)
