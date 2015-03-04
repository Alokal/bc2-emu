WORKDIR = `pwd`

CC = cc
CXX = c++
AR = ar
LD = c++
WINDRES = windres

INC = -I/usr/include -I./source
CFLAGS = -std=gnu++11
RESINC = 
LIBDIR = -L/usr/lib
LIB = /usr/lib/libboost_system.so /usr/lib/libboost_filesystem.so /usr/lib/libboost_random.so /usr/lib/libssl.so /usr/lib/libcrypto.so
LDFLAGS = -lpthread

INC_DEBUG = $(INC)
CFLAGS_DEBUG = $(CFLAGS) -g
RESINC_DEBUG = $(RESINC)
RCFLAGS_DEBUG = $(RCFLAGS)
LIBDIR_DEBUG = $(LIBDIR)
LIB_DEBUG = $(LIB)
LDFLAGS_DEBUG = $(LDFLAGS)
OBJDIR_DEBUG = obj/Debug
DEP_DEBUG = 
OUT_DEBUG = Debug/mase_bc2

INC_RELEASE = $(INC)
CFLAGS_RELEASE = $(CFLAGS) -march=native -O3 -funroll-loops 
RESINC_RELEASE = $(RESINC)
RCFLAGS_RELEASE = $(RCFLAGS)
LIBDIR_RELEASE = $(LIBDIR)
LIB_RELEASE = $(LIB)
LDFLAGS_RELEASE = $(LDFLAGS) -s
OBJDIR_RELEASE = obj/Release
DEP_RELEASE = 
OUT_RELEASE = Release/mase_bc2

OBJ_DEBUG = $(OBJDIR_DEBUG)/source/Network/TcpConnection.o $(OBJDIR_DEBUG)/source/Network/Http/RequestHandler.o $(OBJDIR_DEBUG)/source/Network/Http/RequestParser.o $(OBJDIR_DEBUG)/source/Network/HttpServer.o $(OBJDIR_DEBUG)/source/Network/Packet.o $(OBJDIR_DEBUG)/source/Network/Http/Reply.o $(OBJDIR_DEBUG)/source/Network/TcpConnectionSSL.o $(OBJDIR_DEBUG)/source/Network/TcpServer.o $(OBJDIR_DEBUG)/source/Network/UdpServer.o $(OBJDIR_DEBUG)/source/Base64.o $(OBJDIR_DEBUG)/source/Framework/Config.o $(OBJDIR_DEBUG)/source/Framework/Database.o $(OBJDIR_DEBUG)/source/Framework/Framework.o $(OBJDIR_DEBUG)/source/Framework/GameClient.o $(OBJDIR_DEBUG)/main.o $(OBJDIR_DEBUG)/source/Framework/GameServer.o $(OBJDIR_DEBUG)/source/Framework/Logger.o $(OBJDIR_DEBUG)/source/Framework/Stats.o $(OBJDIR_DEBUG)/source/Network/Http/HttpConnection.o

OBJ_RELEASE = $(OBJDIR_RELEASE)/source/Network/TcpConnection.o $(OBJDIR_RELEASE)/source/Network/Http/RequestHandler.o $(OBJDIR_RELEASE)/source/Network/Http/RequestParser.o $(OBJDIR_RELEASE)/source/Network/HttpServer.o $(OBJDIR_RELEASE)/source/Network/Packet.o $(OBJDIR_RELEASE)/source/Network/Http/Reply.o $(OBJDIR_RELEASE)/source/Network/TcpConnectionSSL.o $(OBJDIR_RELEASE)/source/Network/TcpServer.o $(OBJDIR_RELEASE)/source/Network/UdpServer.o $(OBJDIR_RELEASE)/source/Base64.o $(OBJDIR_RELEASE)/source/Framework/Config.o $(OBJDIR_RELEASE)/source/Framework/Database.o $(OBJDIR_RELEASE)/source/Framework/Framework.o $(OBJDIR_RELEASE)/source/Framework/GameClient.o $(OBJDIR_RELEASE)/main.o $(OBJDIR_RELEASE)/source/Framework/GameServer.o $(OBJDIR_RELEASE)/source/Framework/Logger.o $(OBJDIR_RELEASE)/source/Framework/Stats.o $(OBJDIR_RELEASE)/source/Network/Http/HttpConnection.o

all: debug release

clean: clean_debug clean_release

before_debug: 
	test -d Debug || mkdir -p Debug
	test -d $(OBJDIR_DEBUG)/source/Network || mkdir -p $(OBJDIR_DEBUG)/source/Network
	test -d $(OBJDIR_DEBUG)/source/Network/Http || mkdir -p $(OBJDIR_DEBUG)/source/Network/Http
	test -d $(OBJDIR_DEBUG)/source || mkdir -p $(OBJDIR_DEBUG)/source
	test -d $(OBJDIR_DEBUG)/source/Framework || mkdir -p $(OBJDIR_DEBUG)/source/Framework
	test -d $(OBJDIR_DEBUG) || mkdir -p $(OBJDIR_DEBUG)

after_debug: 

debug: before_debug out_debug after_debug

out_debug: before_debug $(OBJ_DEBUG) $(DEP_DEBUG)
	$(LD) $(LIBDIR_DEBUG) -o $(OUT_DEBUG) $(OBJ_DEBUG)  $(LDFLAGS_DEBUG) $(LIB_DEBUG)

$(OBJDIR_DEBUG)/source/Network/TcpConnection.o: source/Network/TcpConnection.cpp
	$(CXX) $(CFLAGS_DEBUG) $(INC_DEBUG) -c source/Network/TcpConnection.cpp -o $(OBJDIR_DEBUG)/source/Network/TcpConnection.o

$(OBJDIR_DEBUG)/source/Network/Http/RequestHandler.o: source/Network/Http/RequestHandler.cpp
	$(CXX) $(CFLAGS_DEBUG) $(INC_DEBUG) -c source/Network/Http/RequestHandler.cpp -o $(OBJDIR_DEBUG)/source/Network/Http/RequestHandler.o

$(OBJDIR_DEBUG)/source/Network/Http/RequestParser.o: source/Network/Http/RequestParser.cpp
	$(CXX) $(CFLAGS_DEBUG) $(INC_DEBUG) -c source/Network/Http/RequestParser.cpp -o $(OBJDIR_DEBUG)/source/Network/Http/RequestParser.o

$(OBJDIR_DEBUG)/source/Network/HttpServer.o: source/Network/HttpServer.cpp
	$(CXX) $(CFLAGS_DEBUG) $(INC_DEBUG) -c source/Network/HttpServer.cpp -o $(OBJDIR_DEBUG)/source/Network/HttpServer.o

$(OBJDIR_DEBUG)/source/Network/Packet.o: source/Network/Packet.cpp
	$(CXX) $(CFLAGS_DEBUG) $(INC_DEBUG) -c source/Network/Packet.cpp -o $(OBJDIR_DEBUG)/source/Network/Packet.o

$(OBJDIR_DEBUG)/source/Network/Http/Reply.o: source/Network/Http/Reply.cpp
	$(CXX) $(CFLAGS_DEBUG) $(INC_DEBUG) -c source/Network/Http/Reply.cpp -o $(OBJDIR_DEBUG)/source/Network/Http/Reply.o

$(OBJDIR_DEBUG)/source/Network/TcpConnectionSSL.o: source/Network/TcpConnectionSSL.cpp
	$(CXX) $(CFLAGS_DEBUG) $(INC_DEBUG) -c source/Network/TcpConnectionSSL.cpp -o $(OBJDIR_DEBUG)/source/Network/TcpConnectionSSL.o

$(OBJDIR_DEBUG)/source/Network/TcpServer.o: source/Network/TcpServer.cpp
	$(CXX) $(CFLAGS_DEBUG) $(INC_DEBUG) -c source/Network/TcpServer.cpp -o $(OBJDIR_DEBUG)/source/Network/TcpServer.o

$(OBJDIR_DEBUG)/source/Network/UdpServer.o: source/Network/UdpServer.cpp
	$(CXX) $(CFLAGS_DEBUG) $(INC_DEBUG) -c source/Network/UdpServer.cpp -o $(OBJDIR_DEBUG)/source/Network/UdpServer.o

$(OBJDIR_DEBUG)/source/Base64.o: source/Base64.cpp
	$(CXX) $(CFLAGS_DEBUG) $(INC_DEBUG) -c source/Base64.cpp -o $(OBJDIR_DEBUG)/source/Base64.o

$(OBJDIR_DEBUG)/source/Framework/Config.o: source/Framework/Config.cpp
	$(CXX) $(CFLAGS_DEBUG) $(INC_DEBUG) -c source/Framework/Config.cpp -o $(OBJDIR_DEBUG)/source/Framework/Config.o

$(OBJDIR_DEBUG)/source/Framework/Database.o: source/Framework/Database.cpp
	$(CXX) $(CFLAGS_DEBUG) $(INC_DEBUG) -c source/Framework/Database.cpp -o $(OBJDIR_DEBUG)/source/Framework/Database.o

$(OBJDIR_DEBUG)/source/Framework/Framework.o: source/Framework/Framework.cpp
	$(CXX) $(CFLAGS_DEBUG) $(INC_DEBUG) -c source/Framework/Framework.cpp -o $(OBJDIR_DEBUG)/source/Framework/Framework.o

$(OBJDIR_DEBUG)/source/Framework/GameClient.o: source/Framework/GameClient.cpp
	$(CXX) $(CFLAGS_DEBUG) $(INC_DEBUG) -c source/Framework/GameClient.cpp -o $(OBJDIR_DEBUG)/source/Framework/GameClient.o

$(OBJDIR_DEBUG)/main.o: main.cpp
	$(CXX) $(CFLAGS_DEBUG) $(INC_DEBUG) -c main.cpp -o $(OBJDIR_DEBUG)/main.o

$(OBJDIR_DEBUG)/source/Framework/GameServer.o: source/Framework/GameServer.cpp
	$(CXX) $(CFLAGS_DEBUG) $(INC_DEBUG) -c source/Framework/GameServer.cpp -o $(OBJDIR_DEBUG)/source/Framework/GameServer.o

$(OBJDIR_DEBUG)/source/Framework/Logger.o: source/Framework/Logger.cpp
	$(CXX) $(CFLAGS_DEBUG) $(INC_DEBUG) -c source/Framework/Logger.cpp -o $(OBJDIR_DEBUG)/source/Framework/Logger.o

$(OBJDIR_DEBUG)/source/Framework/Stats.o: source/Framework/Stats.cpp
	$(CXX) $(CFLAGS_DEBUG) $(INC_DEBUG) -c source/Framework/Stats.cpp -o $(OBJDIR_DEBUG)/source/Framework/Stats.o

$(OBJDIR_DEBUG)/source/Network/Http/HttpConnection.o: source/Network/Http/HttpConnection.cpp
	$(CXX) $(CFLAGS_DEBUG) $(INC_DEBUG) -c source/Network/Http/HttpConnection.cpp -o $(OBJDIR_DEBUG)/source/Network/Http/HttpConnection.o

clean_debug: 
	rm -f $(OBJ_DEBUG) $(OUT_DEBUG)
	rm -rf Debug
	rm -rf $(OBJDIR_DEBUG)/source/Network
	rm -rf $(OBJDIR_DEBUG)/source/Network/Http
	rm -rf $(OBJDIR_DEBUG)/source
	rm -rf $(OBJDIR_DEBUG)/source/Framework
	rm -rf $(OBJDIR_DEBUG)

before_release: 
	test -d Release || mkdir -p Release
	test -d $(OBJDIR_RELEASE)/source/Network || mkdir -p $(OBJDIR_RELEASE)/source/Network
	test -d $(OBJDIR_RELEASE)/source/Network/Http || mkdir -p $(OBJDIR_RELEASE)/source/Network/Http
	test -d $(OBJDIR_RELEASE)/source || mkdir -p $(OBJDIR_RELEASE)/source
	test -d $(OBJDIR_RELEASE)/source/Framework || mkdir -p $(OBJDIR_RELEASE)/source/Framework
	test -d $(OBJDIR_RELEASE) || mkdir -p $(OBJDIR_RELEASE)

after_release: 

release: before_release out_release after_release

out_release: before_release $(OBJ_RELEASE) $(DEP_RELEASE)
	$(LD) $(LIBDIR_RELEASE) -o $(OUT_RELEASE) $(OBJ_RELEASE)  $(LDFLAGS_RELEASE) $(LIB_RELEASE)

$(OBJDIR_RELEASE)/source/Network/TcpConnection.o: source/Network/TcpConnection.cpp
	$(CXX) $(CFLAGS_RELEASE) $(INC_RELEASE) -c source/Network/TcpConnection.cpp -o $(OBJDIR_RELEASE)/source/Network/TcpConnection.o

$(OBJDIR_RELEASE)/source/Network/Http/RequestHandler.o: source/Network/Http/RequestHandler.cpp
	$(CXX) $(CFLAGS_RELEASE) $(INC_RELEASE) -c source/Network/Http/RequestHandler.cpp -o $(OBJDIR_RELEASE)/source/Network/Http/RequestHandler.o

$(OBJDIR_RELEASE)/source/Network/Http/RequestParser.o: source/Network/Http/RequestParser.cpp
	$(CXX) $(CFLAGS_RELEASE) $(INC_RELEASE) -c source/Network/Http/RequestParser.cpp -o $(OBJDIR_RELEASE)/source/Network/Http/RequestParser.o

$(OBJDIR_RELEASE)/source/Network/HttpServer.o: source/Network/HttpServer.cpp
	$(CXX) $(CFLAGS_RELEASE) $(INC_RELEASE) -c source/Network/HttpServer.cpp -o $(OBJDIR_RELEASE)/source/Network/HttpServer.o

$(OBJDIR_RELEASE)/source/Network/Packet.o: source/Network/Packet.cpp
	$(CXX) $(CFLAGS_RELEASE) $(INC_RELEASE) -c source/Network/Packet.cpp -o $(OBJDIR_RELEASE)/source/Network/Packet.o

$(OBJDIR_RELEASE)/source/Network/Http/Reply.o: source/Network/Http/Reply.cpp
	$(CXX) $(CFLAGS_RELEASE) $(INC_RELEASE) -c source/Network/Http/Reply.cpp -o $(OBJDIR_RELEASE)/source/Network/Http/Reply.o

$(OBJDIR_RELEASE)/source/Network/TcpConnectionSSL.o: source/Network/TcpConnectionSSL.cpp
	$(CXX) $(CFLAGS_RELEASE) $(INC_RELEASE) -c source/Network/TcpConnectionSSL.cpp -o $(OBJDIR_RELEASE)/source/Network/TcpConnectionSSL.o

$(OBJDIR_RELEASE)/source/Network/TcpServer.o: source/Network/TcpServer.cpp
	$(CXX) $(CFLAGS_RELEASE) $(INC_RELEASE) -c source/Network/TcpServer.cpp -o $(OBJDIR_RELEASE)/source/Network/TcpServer.o

$(OBJDIR_RELEASE)/source/Network/UdpServer.o: source/Network/UdpServer.cpp
	$(CXX) $(CFLAGS_RELEASE) $(INC_RELEASE) -c source/Network/UdpServer.cpp -o $(OBJDIR_RELEASE)/source/Network/UdpServer.o

$(OBJDIR_RELEASE)/source/Base64.o: source/Base64.cpp
	$(CXX) $(CFLAGS_RELEASE) $(INC_RELEASE) -c source/Base64.cpp -o $(OBJDIR_RELEASE)/source/Base64.o

$(OBJDIR_RELEASE)/source/Framework/Config.o: source/Framework/Config.cpp
	$(CXX) $(CFLAGS_RELEASE) $(INC_RELEASE) -c source/Framework/Config.cpp -o $(OBJDIR_RELEASE)/source/Framework/Config.o

$(OBJDIR_RELEASE)/source/Framework/Database.o: source/Framework/Database.cpp
	$(CXX) $(CFLAGS_RELEASE) $(INC_RELEASE) -c source/Framework/Database.cpp -o $(OBJDIR_RELEASE)/source/Framework/Database.o

$(OBJDIR_RELEASE)/source/Framework/Framework.o: source/Framework/Framework.cpp
	$(CXX) $(CFLAGS_RELEASE) $(INC_RELEASE) -c source/Framework/Framework.cpp -o $(OBJDIR_RELEASE)/source/Framework/Framework.o

$(OBJDIR_RELEASE)/source/Framework/GameClient.o: source/Framework/GameClient.cpp
	$(CXX) $(CFLAGS_RELEASE) $(INC_RELEASE) -c source/Framework/GameClient.cpp -o $(OBJDIR_RELEASE)/source/Framework/GameClient.o

$(OBJDIR_RELEASE)/main.o: main.cpp
	$(CXX) $(CFLAGS_RELEASE) $(INC_RELEASE) -c main.cpp -o $(OBJDIR_RELEASE)/main.o

$(OBJDIR_RELEASE)/source/Framework/GameServer.o: source/Framework/GameServer.cpp
	$(CXX) $(CFLAGS_RELEASE) $(INC_RELEASE) -c source/Framework/GameServer.cpp -o $(OBJDIR_RELEASE)/source/Framework/GameServer.o

$(OBJDIR_RELEASE)/source/Framework/Logger.o: source/Framework/Logger.cpp
	$(CXX) $(CFLAGS_RELEASE) $(INC_RELEASE) -c source/Framework/Logger.cpp -o $(OBJDIR_RELEASE)/source/Framework/Logger.o

$(OBJDIR_RELEASE)/source/Framework/Stats.o: source/Framework/Stats.cpp
	$(CXX) $(CFLAGS_RELEASE) $(INC_RELEASE) -c source/Framework/Stats.cpp -o $(OBJDIR_RELEASE)/source/Framework/Stats.o

$(OBJDIR_RELEASE)/source/Network/Http/HttpConnection.o: source/Network/Http/HttpConnection.cpp
	$(CXX) $(CFLAGS_RELEASE) $(INC_RELEASE) -c source/Network/Http/HttpConnection.cpp -o $(OBJDIR_RELEASE)/source/Network/Http/HttpConnection.o

clean_release: 
	rm -f $(OBJ_RELEASE) $(OUT_RELEASE)
	rm -rf Release
	rm -rf $(OBJDIR_RELEASE)/source/Network
	rm -rf $(OBJDIR_RELEASE)/source/Network/Http
	rm -rf $(OBJDIR_RELEASE)/source
	rm -rf $(OBJDIR_RELEASE)/source/Framework
	rm -rf $(OBJDIR_RELEASE)

.PHONY: before_debug after_debug clean_debug before_release after_release clean_release

