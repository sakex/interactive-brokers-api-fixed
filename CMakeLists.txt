if (NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE Release)
endif ()

set(CMAKE_CXX_FLAGS_DEBUG "-g")
set(CMAKE_CXX_FLAGS_RELEASE "-O3")

set(CMAKE_CXX_STANDARD 14)

set(INTERACTIVE_BROKER_SOURCES
        client/bar.h
        client/CommissionReport.h
        client/CommonDefs.h
        client/ContractCondition.cpp
        client/ContractCondition.h
        client/Contract.h
        client/DefaultEWrapper.cpp
        client/DefaultEWrapper.h
        client/DepthMktDataDescription.h
        client/EClient.cpp
        client/EClient.h
        client/EClientMsgSink.h
        client/EClientSocket.cpp
        client/EClientSocket.h
        client/EDecoder.cpp
        client/EDecoder.h
        client/EMessage.cpp
        client/EMessage.h
        client/EMutex.cpp
        client/EMutex.h
        client/EOrderDecoder.cpp
        client/EOrderDecoder.h
        client/EPosixClientSocketPlatform.h
        client/EReader.cpp
        client/EReader.h
        client/EReaderOSSignal.cpp
        client/EReaderOSSignal.h
        client/EReaderSignal.h
        client/ESocket.cpp
        client/ESocket.h
        client/ETransport.h
        client/EWrapper.h
        client/EWrapper_prototypes.h
        client/executioncondition.cpp
        client/executioncondition.h
        client/Execution.h
        client/FamilyCode.h
        client/HistogramEntry.h
        client/HistoricalTickBidAsk.h
        client/HistoricalTick.h
        client/HistoricalTickLast.h
        client/IExternalizable.h
        client/MarginCondition.cpp
        client/MarginCondition.h
        client/NewsProvider.h
        client/OperatorCondition.cpp
        client/OperatorCondition.h
        client/OrderCondition.cpp
        client/OrderCondition.h
        client/Order.h
        client/OrderState.h
        client/PercentChangeCondition.cpp
        client/PercentChangeCondition.h
        client/platformspecific.h
        client/PriceCondition.cpp
        client/PriceCondition.h
        client/PriceIncrement.h
        client/resource.h
        client/ScannerSubscription.h
        client/SoftDollarTier.cpp
        client/SoftDollarTier.h
        client/StdAfx.cpp
        client/StdAfx.h
        client/TagValue.h
        client/TickAttribBidAsk.h
        client/TickAttrib.h
        client/TickAttribLast.h
        client/TimeCondition.cpp
        client/TimeCondition.h
        client/TwsSocketClientErrors.h
        client/VolumeCondition.cpp
        client/VolumeCondition.h
        client/)

add_library(IB)
target_include_directories(IB PRIVATE client)
target_sources(IB PRIVATE ${INTERACTIVE_BROKER_SOURCES})