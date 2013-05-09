CC = gcc
CFLAGS = -g -I./
SRCCLIENT = .
SRCSERVER = .
BINCLIENT = bin/client
BINSERVER = bin/server
OBJCLIENT = obj
OBJSERVER = obj
OBJECTSCLIENT = ${OBJCLIENT}/commons.o ${OBJCLIENT}/client_ftp_functions.o ${OBJCLIENT}/file_transfer_functions.o ${OBJCLIENT}/client_ftp.o
OBJECTSSERVER = ${OBJSERVER}/commons.o ${OBJSERVER}/server_ftp_functions.o ${OBJSERVER}/file_transfer_functions.o ${OBJSERVER}/server_ftp.o
EXECUTABLECLIENT = ${BINCLIENT}/client_ftp.out
EXECUTABLESERVER = ${BINSERVER}/server_ftp.out

all: client server

client: commons.o client_ftp_functions.o file_transfer_functions.o client_ftp.o
	gcc ${CFLAGS} $^ -o client_ftp.out

${OBJCLIENT}/%.o:	${SRCCLIENT}/%.c
	${CC} ${CFLAGS} -c $< -o $@



clean:
	rm -f ${OBJCLIENT}/*.o
	rm -f ${BINCLIENT}/*.out
	
