CMAKE_MINIMUM_REQUIRED(VERSION 2.8.10)
PROJECT(zecpp CXX)

SET(CMAKE_CXX_FLAGS "-std=c++11")

SET(OUTPUT_DIR ${CMAKE_BINARY_DIR}/bin)
SET(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${OUTPUT_DIR})
SET(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${OUTPUT_DIR})
SET(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${OUTPUT_DIR})

ADD_EXECUTABLE(asyncsrv asyncsrv.cpp)
TARGET_LINK_LIBRARIES(asyncsrv zmq pthread)

ADD_EXECUTABLE(hwclient hwclient.cpp)
TARGET_LINK_LIBRARIES(hwclient zmq)

ADD_EXECUTABLE(hwserver hwserver.cpp)
TARGET_LINK_LIBRARIES(hwserver zmq)

ADD_EXECUTABLE(identity identity.cpp zhelpers.hpp)
TARGET_LINK_LIBRARIES(identity zmq)

ADD_EXECUTABLE(interrupt interrupt.cpp)
TARGET_LINK_LIBRARIES(interrupt zmq)

ADD_EXECUTABLE(lbbroker2 lbbroker2.cpp)
TARGET_LINK_LIBRARIES(lbbroker2 zmq czmq)

ADD_EXECUTABLE(lbbroker lbbroker.cpp)
TARGET_LINK_LIBRARIES(lbbroker zmq pthread)

ADD_EXECUTABLE(lpclient lpclient.cpp)
TARGET_LINK_LIBRARIES(lpclient zmq)

ADD_EXECUTABLE(lpserver lpserver.cpp)
TARGET_LINK_LIBRARIES(lpserver zmq)

ADD_EXECUTABLE(mdbroker mdbroker.cpp)
TARGET_LINK_LIBRARIES(mdbroker zmq)

ADD_EXECUTABLE(mdclient2 mdclient2.cpp)
TARGET_LINK_LIBRARIES(mdclient2 zmq)

ADD_EXECUTABLE(mdclient mdclient.cpp)
TARGET_LINK_LIBRARIES(mdclient zmq)

ADD_EXECUTABLE(mdworker mdworker.cpp)
TARGET_LINK_LIBRARIES(mdworker zmq)

ADD_EXECUTABLE(msgqueue msgqueue.cpp)
TARGET_LINK_LIBRARIES(msgqueue zmq)

ADD_EXECUTABLE(mspoller mspoller.cpp)
TARGET_LINK_LIBRARIES(mspoller zmq)

ADD_EXECUTABLE(msreader msreader.cpp)
TARGET_LINK_LIBRARIES(msreader zmq)

ADD_EXECUTABLE(mtrelay mtrelay.cpp)
TARGET_LINK_LIBRARIES(mtrelay zmq pthread)

ADD_EXECUTABLE(mtserver mtserver.cpp)
TARGET_LINK_LIBRARIES(mtserver zmq pthread)

ADD_EXECUTABLE(ppqueue ppqueue.cpp)
TARGET_LINK_LIBRARIES(ppqueue zmq)

ADD_EXECUTABLE(ppworker ppworker.cpp)
TARGET_LINK_LIBRARIES(ppworker zmq)

ADD_EXECUTABLE(psenvpub psenvpub.cpp)
TARGET_LINK_LIBRARIES(psenvpub zmq)

ADD_EXECUTABLE(psenvsub psenvsub.cpp)
TARGET_LINK_LIBRARIES(psenvsub zmq)

ADD_EXECUTABLE(rrbroker rrbroker.cpp)
TARGET_LINK_LIBRARIES(rrbroker zmq)

ADD_EXECUTABLE(rrclient rrclient.cpp)
TARGET_LINK_LIBRARIES(rrclient zmq)

ADD_EXECUTABLE(rrworker rrworker.cpp)
TARGET_LINK_LIBRARIES(rrworker zmq)

ADD_EXECUTABLE(rtdealer rtdealer.cpp)
TARGET_LINK_LIBRARIES(rtdealer zmq pthread)

ADD_EXECUTABLE(rtreq rtreq.cpp)
TARGET_LINK_LIBRARIES(rtreq zmq pthread)

ADD_EXECUTABLE(spqueue spqueue.cpp)
TARGET_LINK_LIBRARIES(spqueue zmq)

ADD_EXECUTABLE(spworker spworker.cpp)
TARGET_LINK_LIBRARIES(spworker zmq)

ADD_EXECUTABLE(suisnail suisnail.cpp)
TARGET_LINK_LIBRARIES(suisnail zmq pthread)

ADD_EXECUTABLE(syncpub syncpub.cpp)
TARGET_LINK_LIBRARIES(syncpub zmq)

ADD_EXECUTABLE(syncsub syncsub.cpp)
TARGET_LINK_LIBRARIES(syncsub zmq)

ADD_EXECUTABLE(tasksink2 tasksink2.cpp)
TARGET_LINK_LIBRARIES(tasksink2 zmq)

ADD_EXECUTABLE(tasksink tasksink.cpp)
TARGET_LINK_LIBRARIES(tasksink zmq)

ADD_EXECUTABLE(taskvent taskvent.cpp)
TARGET_LINK_LIBRARIES(taskvent zmq)

ADD_EXECUTABLE(taskwork2 taskwork2.cpp)
TARGET_LINK_LIBRARIES(taskwork2 zmq)

ADD_EXECUTABLE(taskwork taskwork.cpp)
TARGET_LINK_LIBRARIES(taskwork zmq)

ADD_EXECUTABLE(tripping tripping.cpp)
TARGET_LINK_LIBRARIES(tripping zmq pthread)

ADD_EXECUTABLE(udpping1 udpping1.cpp)
TARGET_LINK_LIBRARIES(udpping1 zmq pthread)

ADD_EXECUTABLE(version version.cpp)
TARGET_LINK_LIBRARIES(version zmq)

ADD_EXECUTABLE(wuclient wuclient.cpp)
TARGET_LINK_LIBRARIES(wuclient zmq)

ADD_EXECUTABLE(wuproxy wuproxy.cpp)
TARGET_LINK_LIBRARIES(wuproxy zmq)

ADD_EXECUTABLE(wuserver wuserver.cpp)
TARGET_LINK_LIBRARIES(wuserver zmq)
