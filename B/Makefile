CC = gcc
CFLAGS = -g -I./
SRCCLIENT = .
SRCSERVER = .
BINCLIENT = bin/client
BINSERVER = bin/server
OBJCLIENT = obj
OBJSERVER = obj
OBJECTSSERVER = ${OBJSERVER}/commons.o ${OBJSERVER}/server_ftp_functions.o ${OBJSERVER}/file_transfer_functions.o ${OBJSERVER}/server_ftp.o
EXECUTABLECLIENT = ${BINCLIENT}/client_ftp.out
EXECUTABLESERVER = ${BINSERVER}/server_ftp.out

all: server

server: commons.o server_ftp_functions.o file_transfer_functions.o server_ftp.o
	gcc ${CFLAGS} $^ -o server_ftp.out


${OBJSERVER}/%.o:	${SRCSERVER}/%.c
	${CC} ${CFLAGS} -c $< -o $@

clean:
	rm -f ${OBJSERVER}/*.o
	rm -f ${BINSERVER}/*.out
